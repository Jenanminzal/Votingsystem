# Votingsystem
from collections import deque
class Voter:
    def __init__(self,name,age,addr):
        self.name=name
        self.age=age
        self.addr=addr
        self.Isvoted=False

class Vote:
    def __iter__(self,id,for_condidate):
        self.id=id
        self.for_condidate=for_condidate

class Condidate:
    def __init__(self,name,position):
        self.name=name
        self.positin=[].append()


def structure():
    return []

def condidate():
    return {}

def vote():
    return []

def add_voter(voter):
    for i in structure():
        if (voter.name!= i):
            return structure().append(voter)

def add_condidate(condidate):
    for i in condidate():
        if (condidate.name!= i):
            return condidate().append(condidate)

def casting_vote(votername,condidatename):
    for i in structure():
        if (votername == i.name & i.Isvoted==True):
            i+=1
            voter=i
            if voter & condidatename in condidate():
                vote =Vote(id=len(structure())+1 ,Vote.for_condidate=condidatename)
                vote().append(vote)
                voter.Isvoted=True
                print(f"Vote casted for {condidatename} by {votername}")
            else:
                print("failed vote ")
        else:
            return


def count_votes():
    result ={condidate():0 for key in condidate()}
    for vote in structure():
        if Vote.for_candidate in result:
            result[Vote.for_candidate] +=1
    return result








