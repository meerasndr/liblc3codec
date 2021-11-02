project('liblc3codec', 'cpp', license: 'Apache-2.0' )
cc = meson.get_compiler('cpp')
CFLAGS=-Werror, -Wmissing-braces -Wno-unused-parameter, -Wno-#warnings, -Wuninitialized, -Wno-self-assign, -Wno-implicit-fallthrough

codec_sources = ['Common/DctIV.cpp', 'Common/Lc3Config.cpp', 'Common/Tables/BandIndexTables.cpp',
 'Common/Tables/LongTermPostfilterCoefficients.cpp', 'Common/Tables/MdctWindows.cpp',
 'Common/Tables/SnsQuantizationTables.cpp', 'Common/Tables/SpectralDataTables.cpp',
 'Common/Tables/TemporalNoiseShapingTables.cpp', 'Encoder/AttackDetector.cpp',
 'Encoder/BitstreamEncoding.cpp', 'Encoder/EncoderTop.cpp', 'Encoder/MdctEnc.cpp',
 'Encoder/SnsQuantization.cpp', 'Encoder/SpectralQuantization.cpp',
 'Encoder/BandwidthDetector.cpp', 'Encoder/EncoderFrame.cpp', 'Encoder/Lc3Encoder.cpp',
 'Encoder/LongTermPostfilter.cpp', 'Encoder/NoiseLevelEstimation.cpp',
 'Encoder/SpectralNoiseShaping.cpp', 'Encoder/TemporalNoiseShaping.cpp',
 'Decoder/ArithmeticDec.cpp', 'Decoder/DecoderTop.cpp', 'Decoder/LongTermPostfilter.cpp',
 'Decoder/PacketLossConcealment.cpp', 'Decoder/SpectralNoiseShaping.cpp', 'Decoder/DecoderFrame.cpp',
 'Decoder/MPVQ.cpp', 'Decoder/SideInformation.cpp', 'Decoder/ResidualSpectrum.cpp',
 'Decoder/BitReader.cpp', 'Decoder/Lc3Decoder.cpp', 'Decoder/MdctDec.cpp',
 'Decoder/SideInformation.hpp'
 ]

lc3codec = library('lc3codec',
  codec_sources,
  install: true,
  install_dir: plugins_install_dir,
  )

incdir = include_directories('Api', 'Common', 'Common/Tables', 'Common/KissFft, TestSupport')
