Ton code est plutôt propre avec des commentaires et tu as bien compris la logique de la séparation App / Data.
Maintenant il y a plusieurs soucis: l'organisation de la fenêtre n'est pas très jolie (les boutons sont en dehors), ce que tu peux régler en changeant les paramètres de `.grid()`; et les boutons ne fonctionnnent pas. Pour les boutons, tu dois fournir une fonction avec un paramètre `event`possible, donc cela donne quelque chose comme ca:
`button = Button(root, "Hello", command=self.click)`
avec la fonction suivante:
`def click(self, event): ...`
C'est dommage car le reste du code fonctionne, mais du coup les fonctionnalités à l'écran ne sont pas trop présentes.
