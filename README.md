# TD1
#tirage = ['b', 'p', 'd', 'w', 's', 'y', 'w', 'i']


liste=[]
f=open("frenchssanccent.dic",'r')
for ligne in f:
    liste.append(ligne[0:len(ligne)-1])
f.close()
#exercice 1-2
def mots(tirage):
#d'abord trouver tous les mots possibles
    motspossibles=[]
    for mot in liste:
        liste2=[]
        for lettre in list(mot):
            if lettre in tirage and lettre not in liste2:
                liste2.append(lettre)
        if list(liste2)==mot:
            motspossibles.append(mot)
    return(motspossibles)

def long(tirage):
    L= mots(tirage)

    n= len(list(L[0]):
    motmax=L[0]
        for k in range(1,len(L)]:
            if len(L[k])>=n:
                motmax=L[k]
                n=len(list(L[k])
    return motmax


#exercice 3

point = {'a': 1,'b': 3,'c': 3,'d': 2,'e': 1,'f': 4,'g': 2,'h': 4,'i': 1,'j': 8,'k': 10,'l': 1,'m': 2,'n': 1,'o': 1,'p': 3,'q': 8,'r': 1,'s': 1,'t': 1,'u': 1,'v': 4,'w': 10,'x': 10,'y': 10,'z': 10}

def pointmot(mot):
    Liste=list(mot)
    pt=0
    for elt in Liste:
        pt=pt+point[elt]
    return pt

def pointmax(tirage):
    L=mots(tirage):
        motmax = L[0]
        point_max=pointmot(L[0])
    for k in range(1,len(L)):
        if pt(L[k])>point_max::
            point_max=pointmot(L[k])
            motmax=L[k]
    return [motmax,point_max]



#exercice 4

#alphabetjoker=['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z','?']
#on ajoute une nouvelle fonction qui verifie si ? appartient à notre liste de tirage et si oui, on va s'assurer que le joker a été utilisé qu'une seule et unique fois dans notre mot et que ce dernier même remplacé par une lettre vaudra
#toujours un score nul puis on remplace le joker par toutes les lettre tour à tour dans notre tirage pour connaitre
#si le mot du lexique appartient aux mots possibles et on calcule le mot avec le nombre de score en s'assurant que
#la lettre remplaçant le joker n'a pas été comptée
