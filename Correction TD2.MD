D'un point de vue global, ton fichier est plutôt propre et bien écrit, même s'il manque quelques jeux de tests et de la documentation. Tu sembles avoir compris le principe de classe et d'object.

## Exercice 1

Si jamais tu envoie un polynome avec un coefficient constant égal à 0, tu aura deux soucis: le zero va être affiché, et le monôme d'ordre 1 ne sera pas affiché (par exemple si tu test `Polynome([0,1,2])`).
De la même manière, si tu envoie `Polynome([1,0,1,2])`, le degré d'ordre 2 ne sera pas affiché.
Pour résoudre ces problèmes (et avoir un code plus propre), une manière de faire est d'avoir une seule boucle `for` qui parcourt tous tes termes, et à l'intérieur de faire tes tests sans se baser sur le terme d'avant: est-ce que le coefficient est nul, est ce qu'il est positif ou non, est-ce qu'il est constant, etc. 
Ainsi, tu n'oubliera vraiment aucun terme, et pour pallier au souci des `+ -` qui peut arriver, tu peux utiliser la fonction `replace`: par exemple `"a + -b".replace("+ -","- ")` donne `"a - b"`.
La fonction `add` me semble correcte.

## Exercice 2

Ton code a plusieurs soucis, et notamment le premier est que tu essaie de réinventer le modulo sur les entiers, qui est défini en python par `a % b`, ce qui va te simplifier la tâche.
Je ne suis pas sûr non plus de comprendre ce que tu fais dans ta fonction `__init__` a retrancher une valeur: ici, on veut juste convertir tous les coefficients et les stocker dans une liste, et aussi stocker les paramètres n et q que l'on t'a passé.

Pour la fonction `rescale`, je pense aussi que tu t'emmêles: ici, le but est de repasser tous les coefficients modulo `r`, et de renvoyer un nouveau polynôme.

Avec l'opération modulo, je pense que tu te perdra moins dans ton code et tu peux réussir à écrire les fonctions plus proprement et correctement.

Voici le lien du corrigé: https://github.com/thomas-vinet/Mines-TD-PSD/tree/main/TD2