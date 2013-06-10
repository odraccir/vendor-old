Legalese
========
I did not ask permission to put these sources here. Paizo owns a bunch of stuff on Pathfinder and Wizards of the Coast owns a lot of OGL stuff. They own the rights to about everything about these dataset. See below for the boring stuff that is important!
I put here under fair use rules.

How to use?
=====================

1. Install the prerequisites:

    ```bash
    # need these
    apt-get install openjdk-6-jdk ant
    
    # optional, choose one or both
    apt-get install subversion git
    ```

2. Get the sources from the PCGen subversion or from github:

    ```bash
    # subversion
    svn checkout https://pcgen.svn.sourceforge.net/svnroot/pcgen/Trunk/pcgen
    ```

    ```bash
    # github
    git clone https://github.com/pcgen/pcgen-svn
    ```

3. Build the sources:

    ```bash
    ant build
    ```

4. Use data
   ```bash
   md vendor
   cd vendor
   # github
   git clone https://github.com/odraccir/vendor
    ```

5. Enjoy the latest and/or greatest

   ```bash
   ./pcgen.sh
   ```
   
Copyright stuff
===============

Compatibility with the Pathfinder Roleplaying Game requires the Pathfinder Roleplaying Game from Paizo Publishing, LLC. See http://paizo.com/pathfinderRPG for more information on the Pathfinder Roleplaying Game. Paizo Publishing, LLC does not guarantee compatibility, and does not endorse this product.

Pathfinder is a registered trademark of Paizo Publishing, LLC, and the Pathfinder Roleplaying Game and the Pathfinder Roleplaying Game Compatibility Logo are trademarks of Paizo Publishing, LLC, and are used under the Pathfinder Roleplaying Game Compatibility License. See http://paizo.com/pathfinderRPG/compatibility for more information on the compatibility license.

Product Identity: The following items are hereby identified as Product Identity as defined in the Open Game License version 1.0a, Section 1(e), and are not Open Content: All trademarks, registered trademarks, proper names (characters, locations, etc.), dialogue, plots, story lines, locations, characters, artwork and trade dress. (Elements previously designated as Open Game Content or are in the public domain are not included in this declaration.)

Open Content: Except for material designated as Product Identity (see above), the game mechanics of this Fire Mountain Games game product are Open Game Content, as defined in the Open Game License version 1.0a, Section 1(d). No portion of this work other than the material designated as Open Game Content may be reproduced in any form without written permission.
