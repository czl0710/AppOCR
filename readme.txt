open terminal 
cd AppOCR

opencv_createsamples -vec pos.vec -info pos.txt -num 184 -w 80 -h 90
opencv_traincascade -data xml -vec pos.vec -bg ./neg.txt -numPos 184 -numNeg 1840 -numStages 5 -w 80 -h 90 -minHitRate 0.9999 -maxFalseAlarmRate 0.1 -mode ALL