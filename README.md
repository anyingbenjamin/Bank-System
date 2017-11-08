# Bank-System
Bank system assignment
class Bank():
    def __init__(self,Bankid,Name,Location):
        assert type(Bankid)==int and type(Location)==str
        self.Bankid=Bankid
        self.Name=Name
        self.Location=Location
Bank1=Bank(1,'MUK','MAKERERE')
Bank2=Bank(2,'GU','GULU')

class Teller1(Bank):
    def __init__(self,Id,Name):
        assert type(Id)==int
        self.Id=Id
        self.Name=Name




    def CollectMoney(self,amount):
        self.balance+=amount

        print("%d is your balance"%(self.balance))
        print("you were handled by %s"%Teller1A.Name)

    def OpenAccount(self):
        print("%d, %s your account number is %d"%(self.Id,self.Name,self.AccNo))
        print("your branch is %s"%Bank1.Location)


    def CloseAccount(self):
        print("%s, your account is closed from %s" %(self.Name,Bank1.Location))

    def Loanrequest(self):
        if self.balance>4000:
            print("you are legible to getting a loan from %s" %(Bank1.Location))

        else:
            print("request failed")


    def ProvideInfo(self):
        print("Id:%d\nName:%s\nAddress:%s\nPhoneNo:%d\nAccNo:%d\nBranch:%s"%(self.Id,self.Name,self.Address,self.PhoneNo,self.AccNo,Bank1.Location))


    def IssueCard(self):
        print("%s, your ATM is ready,Come and pick it from %s"%(self.Name,Bank1.Location))





class Teller2(Bank):
    def __init__(self,Id,Name):
        assert type(Id)==int
        self.Id=Id
        self.Name=Name
        self.balance=0

    def CollectMoney(self,amount):
        self.balance+=amount
        print("%d is your balance"%(self.balance))
        print("you were handled by %s"%Teller1B.Name)

    def OpenAccount(self):
        print("%d %s your account number is %d"%(self.Id,self.Name,self.AccNo))
        print("your branch is %s"%Bank2.Location)


    def CloseAccount(self):
        print("%s, your account is closed from %s" %(self.Name,Bank2.Location))

    def Loanrequest(self):
        if self.balance>4000:
            print("you are legible to getting a loan from %s" %(Bank2.Location))

        else:
            print("request failed")

    def ProvideInfo(self):
        print("Id:%d\nName:%s\nAddress:%s\nPhoneNo:%d\nAccNo:%d\nBranch:%s"%(self.Id,self.Name,self.Address,self.PhoneNo,self.AccNo,Bank2.Location))

    def IssueCard(self):
        print("%s, your ATM is ready,Come and pick it from %s"%(self.Name,Bank2.Location))


Teller1A=Teller1(4,"Anying")
Teller1B=Teller1(5,"Chilla")
Teller1C=Teller1(6,"weikama")

Teller2A=Teller2(7,"Morine")
Teller2B=Teller2(8,"Aroma")
Teller2C=Teller2(9,"Benjamn")






class CustomerB(Teller2,Bank):
    def __init__(self,Id,Name,Address,PhoneNo,AccNo):


       self.Id=Id
       self.Name=Name
       self.Address=Address
       self.PhoneNo=PhoneNo
       self.AccNo=AccNo
       self.balance=0


    def GeneralInquiry(self):
        print("Id:%d\nName:%s\nAddress:%s\nPhoneNo:%d\nAccNo:%d\nBalance:%d"%(self.Id,self.Name,self.Address,self.PhoneNo,self.AccNo,self.balance))

    def DepositMoney(self,amount):
        assert type(amount)==int

        self.balance+=amount

        print('%d is your balance'%(self.balance))
        print("you were assisted by %s"%Teller2A.Name)


    def WithdrawMoney(self,amount):
        self.balance-=amount
        if self.balance<2000:
            print("Insufficicient funds on your account")
            print("you were assisted by %s"%Teller2A.Name)

        else:
            print("%d is your balance"%(self.balance))
            print("you were assisted by %s"%Teller2A.Name)


    def openAccount(self):
        print("Do you wish to open an account")


    def closeAccount(self):
        print("Your account nolonger exist")


    def applyLoan(self):
        print("Name:%s,AccNo:%d I would like to get a loan from %s"%(self.Name,self.AccNo,Bank2.Location))

    def requestCard(self):
        print("where is my card")


class CustomerA(Teller1,Bank):
    def __init__(self,Id,Name,Address,PhoneNo,AccNo):


       self.Id=Id
       self.Name=Name
       self.Address=Address
       self.PhoneNo=PhoneNo
       self.AccNo=AccNo
       self.balance=0


    def GeneralInquiry(self):
        print("Id:%d\nName:%s\nAddress:%s\nPhoneNo:%d\nAccNo:%d\nBalance:%d"%(self.Id,self.Name,self.Address,self.PhoneNo,self.AccNo,self.balance))

    def DepositMoney(self,amount):
        assert type(amount)==int

        self.balance+=amount

        print('%d is your balance'%(self.balance))
        print("you were assisted by %s"%Teller1A.Name)



    def WithdrawMoney(self,amount):
        self.balance-=amount
        print("%d is your balance"%self.balance)
        '''if self.balance<2000:
            print("Insufficicient funds on your account")
            print("you were assisted by %s"%Teller1A.Name)

        else:
            print("%d is your balance"%(self.balance))
        print("you were assisted by %s"%Teller1A.Name)'''


    def openAccount(self):
        print("Do you wish to open an account")


    def closeAccount(self):
        print("Your account nolonger exist")


    def applyLoan(self):
        print("Name:%s,AccNo:%d I would like to get a loan from %s"%(self.Name,self.AccNo,Bank1.Location))

    def requestCard(self):
        print("where is my card")




class Account(CustomerB,CustomerA):
    def __init__(self,Id,CustomerId):
        self.Id=Id
        self.CustomerId

        print("your account balance is %d"%self.balance)

class Checking(Account):
    def __init__(self,Id,CustomerId):
        self.Id=Id
        self.CustomerId=CustomerId

        print("your account balance is %d"%self.balance)



class Loan(CustomerB,CustomerA):
    def __init__(self,Id,Type,AccountId,CustomerId):
     pass


class Account():
    def __init__(self,Id,CustomerId):
        pass

class Checking():
    def __init__(self,Id,CustomerId):
        pass

class Savings():
    def __init__(self,Id,CustomerId):
        pass





Ben=CustomerA(12,"Jamin","Kampala",800,290)
Titus=CustomerA(12,"Totio","MBALE",789,87)
Daniel=CustomerA(14,"Dan","Kotido",657,98)
Likambu=CustomerA(15,"Joel","ARUA",546,65)
Okello=CustomerA(16,"David","AGAGO",564,42)
Nyakato=CustomerA(17,"Dave","APAC",525,56)
Peter=CustomerA(34,"Diana","MBARARA",574,12)
John=CustomerA(14,"eden","PAKWACH",564,42)
Mary=CustomerA(21,"wills","BUSHENYI",554,42)
Tom=CustomerA(24,"query","KASESE",544,42)



Grass=CustomerB(45,"Davido","SOROTI",524,42)
cyrus=CustomerB(17,"simon","BUKEDIA",700,42)
lodon=CustomerB(17,"peter","MOROTO",400,42)
derrick=CustomerB(17,"washington","GULU",200,52)
carlos=CustomerB(17,"denzel","BUSHENYI",212,99)
martin=CustomerB(17,"desire","IBANDA",678,32)
denis=CustomerB(17,"isaiah","MARACHA",435,55)
alice=CustomerB(17,"arvid","MAYUGE",900,57)
benson=CustomerB(17,"Denid","LYANTONDO",456,11)
nares=CustomerB(17,"Danse","KOTIDO",456,29)

