# CPAN Name  : PerlIO-gzip
# Contributor: Anonymous
# Generator  : CPANPLUS::Dist::Arch 1.11

pkgname='perl-perlio-gzip'
pkgver='0.18'
pkgrel='1'
pkgdesc="Perl extension to provide a PerlIO layer to gzip/gunzip"
arch=('i686' 'x86_64')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl' 'zlib>=1.2.5')
makedepends=()
url='http://search.cpan.org/dist/PerlIO-gzip'
source=('http://search.cpan.org/CPAN/authors/id/N/NW/NWCLARK/PerlIO-gzip-0.18.tar.gz')
md5sums=('933fdf283a0d2739f7630420569e3b24')

build() {
  PERL=/usr/bin/perl
  DIST_DIR="${srcdir}/PerlIO-gzip-0.18"
  export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
    PERL_AUTOINSTALL=--skipdeps                            \
    PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
    PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
    MODULEBUILDRC=/dev/null

  cd "$DIST_DIR"
  $PERL Makefile.PL
  make
  make test
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
