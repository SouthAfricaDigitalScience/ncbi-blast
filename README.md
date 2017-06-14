DIR  |  |# ncbi-blast

Build, Test and Deploy scripts for the NCBI BLAST application.

# Dependencies

NCBI-BLAST can interface with a lot of things. Here's a table of  dependencies or modules and their status in CODE-RADE (FR3)

| Option | Description | in FR3 ? |
| :---------: | :----------------: | :---------: |
| --with-tcheck(=DIR  ) |     build for Intel Thread Checker (in DIR ) |  :negative_squared_cross_mark:  |
| --with-openmp |           enable OpenMP extensions for all projects | :white_check_mark:  |
| --with-ncbi-c=DIR  |        use NCBI C Toolkit installation in DIR  | :negative_squared_cross_mark:  |
| --with-sss=DIR  |           use NCBI SSS installation in DIR  | :negative_squared_cross_mark: |
| --with-z=DIR  |             use zlib installation in DIR  | :white_check_mark:  |
| --with-bz2=DIR  |           use bzlib installation in DIR  | :white_check_mark:  |
| --with-lzo=DIR  |           use LZO installation in DIR  (requires 2.x or up) | :negative_squared_cross_mark: |
| --with-pcre=DIR  |          use PCRE installation in DIR  | :white_check_mark:  |
| --with-gmp=DIR  |           use GMP installation in DIR  | :white_check_mark:  |
| --with-gcrypt=DIR  |        use gcrypt installation in DIR  |  :negative_squared_cross_mark:  |
| --with-nettle=DIR  |        use Nettle installation in DIR  | :negative_squared_cross_mark: |
| --with-gnutls=DIR  |        use GNUTLS installation in DIR  | :white_check_mark: |
| --with-openssl=DIR  |       use OpenSSL installation in DIR  | :white_check_mark:  |
| --with-krb5=DIR  |          use Kerberos 5 installation in DIR  |  :negative_squared_cross_mark: |
| --with-sybase-local=DIR  |  use local SYBASE install (DIR  is optional) | :negative_squared_cross_mark: |
| --with-ftds=DIR  |          use FreeTDS installation in DIR  | :negative_squared_cross_mark:  |
| --with-mysql=DIR  |         use MySQL installation in DIR  | :negative_squared_cross_mark: |
| --with-opengl=DIR  |        use OpenGL installation in DIR  | :negative_squared_cross_mark: |
| --with-mesa=DIR  |          use MESA installation in DIR  | :negative_squared_cross_mark: |
| --with-glut=DIR  |          use GLUT installation in DIR  | :negative_squared_cross_mark: |
| --with-glew=DIR  |        use GLEW installation in DIR  | :negative_squared_cross_mark: |
| --with-wxwidgets=DIR  |    use wxWidgets installation in DIR  | :negative_squared_cross_mark: |
| --with-freetype=DIR  |    use FreeType installation in DIR  | :white_check_mark:  |
| --with-ftgl=DIR  |        use FTGL installation in DIR  | :negative_squared_cross_mark:  |
| --with-fastcgi=DIR  |      use Fast-CGI installation in DIR  | :negative_squared_cross_mark:  |
| --with-bdb=DIR  |          use Berkeley DB installation in DIR  | :negative_squared_cross_mark:  |
| --with-orbacus=DIR  |     use ORBacus installation in DIR  | :negative_squared_cross_mark:  |
| --with-odbc=DIR  |      use ODBC installation in DIR  | :negative_squared_cross_mark:  |
| --with-python=DIR  |    use Python installation in DIR  | :white_check_mark:  |
| --with-perl=DIR  |       use Perl installation in DIR  | :white_check_mark:  |
| --with-jni(=JDK-DIR)  |   build Java bindings (against the JDK in JDK-DIR) | :white_check_mark:  |
| --with-boost=DIR  |       use Boost installation in DIR  | :white_check_mark:  |
| --with-sqlite3=DIR  |     use SQLite 3.x installation in DIR  | :white_check_mark:  |
| --with-icu=DIR  |         use ICU installation in DIR  | ... almost ...  |
| --with-expat=DIR  |       use Expat installation in DIR  | :negative_squared_cross_mark: |
| --with-sablot=DIR  |      use Sablotron installation in DIR  | :negative_squared_cross_mark: |
| --with-libxml=DIR  |      use libxml2 installation in DIR  | :white_check_mark:  |
| --with-libxslt=DIR  |     use libxslt installation in DIR  | :negative_squared_cross_mark: |
| --with-libexslt=DIR  |    use libexslt installation in DIR  | :negative_squared_cross_mark: |
| --with-xerces=DIR  |      use Xerces-C++ installation in DIR  | :negative_squared_cross_mark: |
| --with-xalan=DIR  |       use Xalan-C++ installation in DIR  | :negative_squared_cross_mark: |
| --with-zorba=DIR  |       use Zorba installation in DIR  | :negative_squared_cross_mark: |
| --with-oechem=DIR  |      use OpenEye OEChem installation in DIR  | :negative_squared_cross_mark: |
| --with-sge=DIR  |         use Sun/Univa Grid Engine installation in DIR  | :negative_squared_cross_mark: |
| --with-muparser=DIR  |  use muParser installation in DIR  | :negative_squared_cross_mark: |
| --with-hdf5=DIR  |         use HDF5 installation in DIR  | :white_check_mark:  |
| --with-gif=DIR  |          use lib(un)gif installation in DIR  | :negative_squared_cross_mark: |
| --with-jpeg=DIR  |         use libjpeg installation in DIR  | :white_check_mark:  |
| --with-png=DIR  |          use libpng installation in DIR  | :white_check_mark:  |
| --with-tiff=DIR  |        use libtiff installation in DIR  |   :negative_squared_cross_mark: |
| --with-magic=DIR  |       use libmagic installation in DIR  | :negative_squared_cross_mark: |
| --with-curl=DIR  |        use libcurl installation in DIR  | :white_check_mark:  |
| --with-mimetic=DIR  |      use libmimetic installation in DIR  | :negative_squared_cross_mark: |
| --with-gsoap=DIR  |        use gSOAP++ installation in DIR  | :negative_squared_cross_mark: |
| --with-avro=DIR  |        use Apache Avro installation in DIR  | :negative_squared_cross_mark: |
| --with-cereal=DIR  |       use USC Cereal installation in DIR  | :negative_squared_cross_mark: |
| --with-sasl2=DIR  |        use SASL 2 installation in DIR  | :negative_squared_cross_mark: |
| --with-mongodb=DIR  |      use MongoDB installation in DIR  | :negative_squared_cross_mark: |
| --with-gmock=DIR  |         use Google Mock installation in DIR  | :negative_squared_cross_mark: |
| --with-lapack=DIR  |       use LAPACK installation in DIR  | :white_check_mark:  |
| --with-lmdb=DIR  |          use LMDB installation in DIR | :negative_squared_cross_mark: |
| --with-gbench |           ensure that Genome Workbench can be built | :negative_squared_cross_mark: |
