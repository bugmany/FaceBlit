# FaceBlit: Instant Real-Time Example-Based Style Transfer to Facial Videos

The official implementation of

> **FaceBlit: Instant Real-Time Example-Based Style Transfer to Facial Videos** <br>
_[A. Texler](https://www.linkedin.com/in/aneta-texler/), [O. Texler](https://ondrejtexler.github.io/), [M. Kučera](https://www.linkedin.com/in/kuceram/), [M. Chai](http://www.mlchai.com), and [D. Sýkora](https://dcgi.fel.cvut.cz/home/sykorad/)_ <br>
[:globe_with_meridians: Project Page](https://ondrejtexler.github.io/faceblit/index.html), 
[:page_facing_up: Paper](https://dcgi.fel.cvut.cz/home/sykorad/Texler21-I3D.pdf), 
[:books: BibTeX](https://dcgi.fel.cvut.cz/home/sykorad/Texler21-I3D.bib)

FaceBlit is a system for real-time example-based face video stylization that retains textural details
of the style in a semantically meaningful manner, i.e., strokes used to depict specific features in the style are
present at the appropriate locations in the target image. As compared to previous techniques, our system
preserves the identity of the target subject and runs in real-time without the need for large datasets nor
lengthy training phase. To achieve this, we modify the existing face stylization pipeline of 
[Fišer et al. [2017]](https://dcgi.fel.cvut.cz/home/sykorad/facestyle.html) so that it can quickly generate a set 
of guiding channels that handle identity preservation of the target subject while are still compatible with a faster 
variant of patch-based synthesis algorithm of [Sýkora et al. [2019]](https://dcgi.fel.cvut.cz/home/sykorad/styleblit.html).
Thanks to these improvements we demonstrate a first face stylization pipeline that can instantly transfer
artistic style from a single portrait to the target video at interactive rates even on mobile devices.

![Teaser](docs/teaser.png)

## Build

### Windows
* There is a Visual Studio project in directory *FaceBlit/VS*
* OpenCV version: 4.5.0
  * This repository contains necessary .lib files and includes
  * .dll files need to be downloaded (https://sourceforge.net/projects/opencvlibrary/files/4.5.0/opencv-4.5.0-vc14_vc15.exe/download - pre-built for Windows)
    * _opencv_world450d.dll_ and _opencv_world450.dll_ files are located in _opencv-4.5.0-vc14_vc15/build/x64/vc15/bin_ and are expected in the PATH 
* Dlib version: 19.21
  * It is added to the project as a "Header-only library" - file *FaceBlit/app/src/main/cpp/source.cpp*
### Android
TODO
## Run

### Windows
TODO
### Android
TODO

## Notes
* All CPP sources (except main.cpp) are located in *FaceBlit/app/src/main/cpp*
* Style exemplars (.png) are located in *FaceBlit/app/src/main/res/drawable*
* Files with detected landmarks (.txt) and lookup tables (.bytes) for each style are located in *FaceBlit/app/src/main/res/raw*

## License
The algorithm is not patented. The code is released under the public domain - feel free to use it for research or commercial purposes.

## Citing
If you find _FaceBlit_ useful for your research or work, please use the following BibTeX entry.

    @Article{Texler21-I3D,
        author    = "Aneta Texler and Ond\v{r}ej Texler and Michal Ku\v{c}era and Menglei Chai and Daniel S\'{y}kora",
        title     = "FaceBlit: Instant Real-time Example-based Style Transfer to Facial Videos",
        journal   = "Proceedings of the ACM in Computer Graphics and Interactive Techniques",
        volume    = "4",
        number    = "1",
        year      = "2021",
    }
