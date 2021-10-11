# moleculeN2
spectre émission du second système positif de N2


Télécharger le fichier `n2_2sp`, c'est un exécutable sous linux.

La syntaxe est la suivante 

`./n2_2sp -T TR TV TExc -P LMH -D densite -F (ou -R ou -A) fichier -L L1 L2`

1. **-T** pour les températures, dans l'ordre la température de rotation (TR), puis celle de vibration (TV) et enfin celle d'excitation éectronique (TExc)
2. **-P** pour la fonction d'appareil (gaussienne), donner la valeur de la largeur à mi-hauteur (LMH)
3. **-D** donner la valeur de la densité total de N_2 (densite).
4. **-F** enregistre les résultats dans un fichier dont le nom commencera par fichier. le fichier résultat est enregistré dans le chemin courant de l'exécution du programme
5. **-R** enregistre le fichier résultat dans le répertoire (fichier) du répertoire courant d'où est exécuté le programme
6. **-A** enregistre le fichier résultat dans le répertoire absolu (fichier)
7. **-L** intervalle sur le quel sont effectués les calculs [L1;L2]

**Remarques** 
- Le fichier se termine toujours par `N2_TR_TV_TExc_densite.sp`
- Il faut faire un choix entre -R, -A et -F
- La distribution de Boltzmann est supposée sur les états électronique à TExc, sur les états de vibration à TV et sur les états de rotation à TR, par conséquent les spectres obtenus sont en intensité absolue W/m^{-3}
- Si vous souhaitez normaliser le spectre, alors ajouter l'option **-N l1 l2 In**, avec l1, l2 les bornes de l'intervalle sur lequel sera déterminé l'intensité maximale qui sera fixée à In.


Un exemple d'exécution est disponible sur l'image : `execution.png` et le fichier `spectre1.png` contient la représentation du résultat obtenu.

