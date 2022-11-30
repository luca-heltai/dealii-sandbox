FROM dealii/dealii:master-focal

USER root 

RUN mkdir -p /step-40

ADD step-40.cc /step-40
ADD CMakeLists.txt /step-40

RUN mkdir /build-debug && \
    cd /build-debug && \
    cmake -GNinja ../step-40 -DCMAKE_BUILD_TYPE=Debug && \
    ninja && \
    mv step-40 /usr/bin/step-40 && \
    cd ../ && rm -rf /build-debug

CMD /usr/bin/step-40
