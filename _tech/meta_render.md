# Instructions for efficient rendering using Adobe After Effects

By default, After Effects only uses a single CPU core when rendering regardless of how many cores your computer has. However, by using [After Effect's automated rendering program](https://helpx.adobe.com/after-effects/using/automated-rendering-network-rendering.html), you can use as many cores as you like by running multiple parallel instances of After Effects.

1. After you create your composition, add it to your render queue using the output settings that you normally would. Note your composition's name and your project file's name and close the program.
2. Open terminal (or command prompt if Windows) and type the following to navigate to your After Effects application directory:

   ```
   cd "/Applications/Adobe After Effects CC 2018"/
   ```
   
   or if Windows:
   
   ```
   cd "C:\\Program Files\Adobe\Adobe After Effects CC 2018\Support Files"
   ```
   
   You may need to slightly modify based on your version of After Effects.
3. Now you are able to run the `aerender` process in the command line, e.g.

   ```
   ./aerender -project "/path/to/project.aep" -comp "MyComposition" -s 10 -e 20  -output "/path/to/frames.[#####].png"
   ```
