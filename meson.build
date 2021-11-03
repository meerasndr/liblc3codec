project('liblc3codec', 'cpp', license: 'Apache-2.0' )

codec_sources = [
  'Common/DctIV.cpp',
  'Common/Lc3Config.cpp',
  'Common/Tables/BandIndexTables.cpp',
  'Common/Tables/LongTermPostfilterCoefficients.cpp',
  'Common/Tables/MdctWindows.cpp',
  'Common/Tables/SnsQuantizationTables.cpp',
  'Common/Tables/SpectralDataTables.cpp',
  'Common/Tables/TemporalNoiseShapingTables.cpp',
  'Decoder/ArithmeticDec.cpp',
  'Decoder/BitReader.cpp',
  'Decoder/DecoderFrame.cpp',
  'Decoder/DecoderTop.cpp',
  'Decoder/Lc3Decoder.cpp',
  'Decoder/LongTermPostfilter.cpp',
  'Decoder/MdctDec.cpp',
  'Decoder/MPVQ.cpp',
  'Decoder/PacketLossConcealment.cpp',
  'Decoder/ResidualSpectrum.cpp',
  'Decoder/SpectralNoiseShaping.cpp',
  'Decoder/SideInformation.cpp',
  'Encoder/AttackDetector.cpp',
  'Encoder/BitstreamEncoding.cpp',
  'Encoder/EncoderTop.cpp',
  'Encoder/MdctEnc.cpp',
  'Encoder/SnsQuantization.cpp',
  'Encoder/SpectralQuantization.cpp',
  'Encoder/BandwidthDetector.cpp',
  'Encoder/EncoderFrame.cpp',
  'Encoder/Lc3Encoder.cpp',
  'Encoder/LongTermPostfilter.cpp',
  'Encoder/NoiseLevelEstimation.cpp',
  'Encoder/SpectralNoiseShaping.cpp',
  'Encoder/TemporalNoiseShaping.cpp',
  'TestSupport/DatapointsAndroid.cpp',
]

codec_headers = [
  'Api/Lc3Config.hpp',
  'Api/Lc3Decoder.hpp',
  'Api/Lc3Encoder.hpp',
]

incdir = include_directories(
  'Api',
  'Common',
  'Common/KissFft',
  'Common/Tables',
  'TestSupport',
)

lc3codec = library('lc3codec',
  codec_sources,
  include_directories: incdir,
  install: true,
)

install_headers(codec_headers,
  subdir: 'liblc3codec',
)

pkg = import('pkgconfig')
pkg.generate(lc3codec,
  name: 'liblc3codec',
  description: 'Library for encoding/decoding audio using the LC3 codec',
  subdirs: 'liblc3codec',
)
