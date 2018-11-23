## OpenCV: Open Source Computer Vision Library

### Resources

* Homepage: <http://opencv.org>
* Docs: <http://docs.opencv.org/master/>
* Q&A forum: <http://answers.opencv.org>
* Issue tracking: <https://github.com/opencv/opencv/issues>

### Contributing

Please read the [contribution guidelines](https://github.com/opencv/opencv/wiki/How_to_contribute) before starting work on a pull request.

#### Summary of the guidelines:

* One pull request per issue;
* Choose the right base branch;
* Include tests and documentation;
* Clean up "oops" commits before submitting;
* Follow the [coding style guide](https://github.com/opencv/opencv/wiki/Coding_Style_Guide).

## Compile:
cmake -D BUILD_opencv_gpu=OFF -D BUILD_opencv_apps=OFF -D BUILD_opencv_video=OFF -D BUILD_opencv_videostab=OFF -D BUILD_opencv_stitching=OFF -D BUILD_opencv_superres=OFF -D BUILD_opencv_ts=OFF -D WITH_PNG=ON -D WITH_TIFF=ON -D WITH_JPEG=ON -D WITH_JASPER=ON -D WITH_WEBP=OFF -D WITH_CUDA=OFF -D WITH_1394=OFF -D WITH_FFMPEG=OFF -D WITH_QT=OFF -D WITH_QUICKTIME=OFF -D WITH_LIBV4L=OFF -D WITH_V4L=OFF -D BUILD_TBB=OFF -D WITH_PVAPI=OFF -D BUILD_WITH_DEBUG_INFO=OFF -DBUILD_SHARED_LIBS=NO -D BUILD_NEW_PYTHON_SUPPORT=OFF -D BUILD_TESTS=OFF -D BUILD_PERF_TESTS=OFF -D BUILD_EXAMPLES=OFF -D BUILD_DOCS=OFF -D INSTALL_C_EXAMPLES=OFF -D INSTALL_PYTHON_EXAMPLES=OFF -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -Wno-error=pointer-bool-conversion -Wno-error=-tautological-pointer-compare -Wno-dev ..

#### IF ASM instruction not support, such as AVX2
-D CPU_DISPATCH=SSE4_2,AVX
#### without python
-D BUILD_opencv_python2=OFF
#### merge to a framework
-D BUILD_opencv_world=ON
