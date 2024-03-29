# yue.nicholas@gmail.com

# IlmImfTest

ADD_EXECUTABLE ( IlmImfTest
  compareB44.cpp
  compareDwa.cpp
  compareFloat.cpp
  main.cpp
  testAttributes.cpp
  testBackwardCompatibility.cpp
  testBadTypeAttributes.cpp
  testChannels.cpp
  testCompositeDeepScanLine.cpp
  testCompression.cpp
  testConversion.cpp
  testCopyDeepScanLine.cpp
  testCopyDeepTiled.cpp
  testCopyMultiPartFile.cpp
  testCopyPixels.cpp
  testCustomAttributes.cpp
  testDeepScanLineBasic.cpp
  testDeepScanLineHuge.cpp
  testDeepScanLineMultipleRead.cpp
  testDeepTiledBasic.cpp
  testDwaCompressorSimd.cpp
  testExistingStreams.cpp
  testFutureProofing.cpp
  testHuf.cpp
  testInputPart.cpp
  testIsComplete.cpp
  testLineOrder.cpp
  testLut.cpp
  testMagic.cpp
  testMalformedImages.cpp
  testMultiPartApi.cpp
  testMultiPartFileMixingBasic.cpp
  testMultiPartSharedAttributes.cpp
  testMultiPartThreading.cpp
  testMultiScanlinePartThreading.cpp
  testMultiTiledPartThreading.cpp
  testMultiView.cpp
  testNativeFormat.cpp
  testOptimized.cpp
  testOptimizedInterleavePatterns.cpp
  testPartHelper.cpp
  testPreviewImage.cpp
  testRgba.cpp
  testRgbaThreading.cpp
  testRle.cpp
  testSampleImages.cpp
  testScanLineApi.cpp
  testSharedFrameBuffer.cpp
  testStandardAttributes.cpp
  testTiledCompression.cpp
  testTiledCopyPixels.cpp
  testTiledLineOrder.cpp
  testTiledRgba.cpp
  testTiledYa.cpp
  testWav.cpp
  testXdr.cpp
  testYca.cpp
  testIDManifest.cpp
 )

SET_ILMBASE_INCLUDE_DIRS( IlmImfTest )

ADD_TEST ( TestIlmImf IlmImfTest )
TARGET_LINK_LIBRARIES ( IlmImfTest
  OpenEXR::IlmImf${OPENEXR_TARGET_SUFFIX}
  IlmBase::Half${OPENEXR_TARGET_SUFFIX}
  IlmBase::Iex${OPENEXR_TARGET_SUFFIX}
  IlmBase::Imath${OPENEXR_TARGET_SUFFIX}
  IlmBase::IlmThread${OPENEXR_TARGET_SUFFIX}
  ${PTHREAD_LIB} ${ZLIB_LIBRARIES}
  )
