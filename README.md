## Men haqimda
<!DOCTYPE html>
<html lang="en">
<head>
</head>
<body>
    <h2>Salom mening ismim Tohirboyev Sultonbek. Men Xorazm viloyati Xonqa tumanida yashayman. 
      Hozirda Matematika va IT sohasi bilan shug‘ullanmoqdaman. 
      Kelajakda men eng yaxshi IT mutaxasisi bo'lishni niyat qilganman.
      Men Muhammad Al Xorazmiy vorislari loyihasida Html, CSS , JavaScript va Python dasturlash
      tillarinini to’liq o’rganib chiqqanman.Va men instagram cloni , 
      IT sohalari veb sayti va shunga o’xshash veb saytlarni yaratganman.<h2/>
</body>
</html>

<pre align="center">
████████╗ ██████╗ ██╗  ██╗██╗██████╗  ██████╗ ██╗   ██╗
╚══██╔══╝██╔═══██╗╚██╗██╔╝██║██╔══██╗██╔═══██╗██║   ██║
   ██║   ██║   ██║ ╚███╔╝ ██║██████╔╝██║   ██║██║   ██║
   ██║   ██║   ██║ ██╔██╗ ██║██╔══██╗██║   ██║╚██╗ ██╔╝
   ██║   ╚██████╔╝██╔╝ ██╗██║██║  ██║╚██████╔╝ ╚████╔╝ 
   ╚═╝    ╚═════╝ ╚═╝  ╚═╝╚═╝╚═╝  ╚═╝ ╚═════╝   ╚═══╝  
</pre>

<img src="https://github.com/user-attachments/assets/2127c7c0-3cbb-41f4-849b-18bed46529ca" 
     style="width: 100%; height: auto; display: block; margin: 0; padding: 0;" 
     alt="Rainbow Line">
          
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=250&color=0:000000,50:8A2BE2,100:000000&text=Welcome%20to%20my%20profile!&fontSize=50&fontColor=39FF14&animation=twinkling&fontAlignY=38"/>
</p>

<!--chiziqni kodi-->

<img src="https://github.com/user-attachments/assets/2127c7c0-3cbb-41f4-849b-18bed46529ca" 
     style="width: 100%; height: auto; display: block; margin: 0; padding: 0;" 
     alt="Rainbow Line">
     
<p align="center">
  <img src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/matrix.svg" alt="Matrix animation"/>
</p>
     
name: Generate Matrix Animation

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - name: Generate matrix animation
        uses: Platane/snk@v3
        with:
          github_user_name: YOUR_USERNAME
          outputs: |
            dist/matrix.svg

      - name: Push animation
        uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
