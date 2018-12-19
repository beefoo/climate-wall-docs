# Instructions for efficient rendering using Adobe After Effects

By default, After Effects only uses a single CPU core when rendering regardless of how many cores your computer has. However, by using [After Effect's automated rendering program](https://helpx.adobe.com/after-effects/using/automated-rendering-network-rendering.html), you can use as many cores as you like by running multiple parallel instances of After Effects.

1. After you create your composition, add it to your render queue using the output settings that you normally would. Note your composition's name and your project file's name and close the program.

   Note if you have multiple instances of the same composition with the same name in your queue, AFX will use the settings of the _first_ instance of the composition (not the most recent).  If this is not what you want, clear the queue before adding the composition with the settings you want.

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
   
   In the example above, frames 10 through 20 will be rendered.  Note to replace "MyComposition" to your composition name noted in step one.  And replace the pathnames to the full absolute path to your project and frames. 
   
4. To run multiple processes at once, you'll need to open multiple terminals and target each terminal to a different range of frames. The amount of processes you should run at once depends on your CPU.  For example, if you have an 8-core processor, you should try around 5-6 instances.  In this example, we will render 10,000 frames using 5 processes (2000 frames per process):

   ```
   Process 1:
   ./aerender -project "/path/to/project.aep" -comp "MyComposition" -s 1 -e 2000  -output "/path/to/frames.[#####].png"
   Process 2:
   ./aerender -project "/path/to/project.aep" -comp "MyComposition" -s 2001 -e 4000  -output "/path/to/frames.[#####].png"
   Process 3:
   ./aerender -project "/path/to/project.aep" -comp "MyComposition" -s 4001 -e 6000  -output "/path/to/frames.[#####].png"
   Process 4:
   ./aerender -project "/path/to/project.aep" -comp "MyComposition" -s 6001 -e 8000  -output "/path/to/frames.[#####].png"
   Process 5:
   ./aerender -project "/path/to/project.aep" -comp "MyComposition" -s 8001  -output "/path/to/frames.[#####].png"
   ```
   
   Note that each line represents a different process running in a different terminal.  Also note that the last one omits an "end" frame, so the process will assume that it should render to the end.
