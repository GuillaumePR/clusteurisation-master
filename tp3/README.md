# tp3-conteneurisation

3 optimisations :
- multi-stage build qui sépare les installs et reduit la taille de l’image final
- utiliser node:20-alpine pour une image plus légère et plus rapide (et donc tous les avantages qui vont avec ça)
- 'npm ci' au lieu de 'npm install' : intall basé sur package lock donc build plus rapide 

<img width="1611" height="934" alt="Screenshot 2026-04-01 104021" src="https://github.com/user-attachments/assets/09ffb090-b9e8-49a0-9681-9c80755858ed" />
<img width="844" height="527" alt="Screenshot 2026-04-01 103840" src="https://github.com/user-attachments/assets/a007016b-3d2e-4387-b087-d590148b5cc4" />
<img width="842" height="72" alt="Screenshot 2026-04-01 110608" src="https://github.com/user-attachments/assets/eff7e517-32bc-4a3e-a6f0-f796fe111e78" />
