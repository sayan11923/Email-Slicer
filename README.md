# Email-Slicer
Using python programm i created  a project on email slicer
def email_sclicer(email):
    """
    seperates text before "@" and after "@"
    """
    i=email.index("@")
    return email[:i],email[i+1:]  #returns a tuple containing string before and after "@"


while True:
    email = input("Enter your email: ")
    if "@" in email:
        username,domain=email_sclicer(email)
        print(f"username: {username} and domain: {domain.upper()}")
        break
    else:
        print("Enter your correct Email")
