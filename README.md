# Normalized-Compression-Distance---Zlib
Simple C++ header file with a class that uses the Zlib compression algorithm to calculate Normalized Compression Distance (NCD) values



 This simple class allows you to calculate a
   Normalized Compression Distance (NCD) between
   char* buffers. This class does not help with the
   actual serialization of data into buffers, you'll
   have to handle that yourself.

   This particular implementation uses the
   Zlib compression algorithm. This is a very
   fast compression algorithm, and is appropriate
   for use in cases where speed is of the utmost
   importance.

   The downside of using Zlib for NCD calculations
   is that the two buffers together cannot be bigger
   than 32K bytes. NCD won't work in this case.

   There are better NCD implementations. LZMA compression
   is an excellent NCD compressor to use, but is
   significantly slower than zlib. You avoid the
   size restrictions with LZMA, and it's very
   accurate.

   For more information on NCD, see www.complearn.org.
   They have excellent NCD implementations there.
   CompLearn.org is moving away from
   zlib and gzip implementations to
   a wholly LZMA implementation to save researchers from
   themselves, as numerous studies have ignored the size
   limits associated with various compressors.

   There is no .cpp file for this class, the
   implementation is completely contained in this
   .h file, so it's very easy to add to your software.

   By default, this class uses the fastest Zlib
   compression level. You can change that with
   the function ChangeCompressionLevel. Basically
   you can only choose Z_BEST_SPEED (default),
   or Z_BEST_COMPRESSION.

   Drew Kirkpatrick
   drew.kirkpatrick@gmail.com
