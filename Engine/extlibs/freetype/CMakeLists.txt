#****************************************************************************
# Copyright (c) 2011-2013,WebJet Business Division,CYOU
#  
# http://www.genesis-3d.com.cn
# 
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:

# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.
# 
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
# THE SOFTWARE.
#****************************************************************************


##################################################################################
# Build FreeType2 
##################################################################################


#include folder
SET ( _INCLUDE_ 
		include/ft2build.h
)

#include/freetype folder
SET ( __FREETYPE_
		include/freetype/freetype.h
		include/freetype/ftadvanc.h
		include/freetype/ftbbox.h
		include/freetype/ftbdf.h
		include/freetype/ftbitmap.h
		include/freetype/ftbzip2.h
		include/freetype/ftcache.h
		include/freetype/ftchapters.h
		include/freetype/ftcid.h
		include/freetype/fterrdef.h
		include/freetype/fterrors.h
		include/freetype/ftgasp.h
		include/freetype/ftglyph.h
		include/freetype/ftgxval.h
		include/freetype/ftgzip.h
		include/freetype/ftimage.h
		include/freetype/ftincrem.h
		include/freetype/ftlcdfil.h
		include/freetype/ftlist.h
		include/freetype/ftlzw.h
		include/freetype/ftmac.h
		include/freetype/ftmm.h
		include/freetype/ftmodapi.h
		include/freetype/ftmoderr.h
		include/freetype/ftotval.h
		include/freetype/ftoutln.h
		include/freetype/ftpfr.h
		include/freetype/ftrender.h
		include/freetype/ftsizes.h
		include/freetype/ftsnames.h
		include/freetype/ftstroke.h
		include/freetype/ftsynth.h
		include/freetype/ftsystem.h
		include/freetype/fttrigon.h
		include/freetype/fttypes.h
		include/freetype/ftwinfnt.h
		include/freetype/ftxf86.h
		include/freetype/t1tables.h
		include/freetype/ttnameid.h
		include/freetype/tttables.h
		include/freetype/tttags.h
		include/freetype/ttunpat.h		
)
#include/freetype/config
SET ( ___CONFIG_ 
		include/freetype/config/ftconfig.h
		include/freetype/config/ftheader.h
		include/freetype/config/ftmodule.h
		include/freetype/config/ftoption.h
		include/freetype/config/ftstdlib.h	
)

#include/freetype/internal
SET ( ___INTERNAL 
		include/freetype/internal/autohint.h
		include/freetype/internal/ftcalc.h
		include/freetype/internal/ftdebug.h
		include/freetype/internal/ftdriver.h
		include/freetype/internal/ftgloadr.h
		include/freetype/internal/ftmemory.h
		include/freetype/internal/ftobjs.h
		include/freetype/internal/ftpic.h
		include/freetype/internal/ftrfork.h
		include/freetype/internal/ftserv.h
		include/freetype/internal/ftstream.h
		include/freetype/internal/fttrace.h
		include/freetype/internal/ftvalid.h
		include/freetype/internal/internal.h
		include/freetype/internal/psaux.h
		include/freetype/internal/pshints.h
		include/freetype/internal/sfnt.h
		include/freetype/internal/t1types.h
		include/freetype/internal/tttypes.h	

)
#include/freetype/internal/services
SET ( ____SERVICES
		include/freetype/internal/services/svbdf.h
		include/freetype/internal/services/svcid.h
		include/freetype/internal/services/svgldict.h
		include/freetype/internal/services/svgxval.h
		include/freetype/internal/services/svkern.h
		include/freetype/internal/services/svmm.h
		include/freetype/internal/services/svotval.h
		include/freetype/internal/services/svpfr.h
		include/freetype/internal/services/svpostnm.h
		include/freetype/internal/services/svpscmap.h
		include/freetype/internal/services/svpsinfo.h
		include/freetype/internal/services/svsfnt.h
		include/freetype/internal/services/svttcmap.h
		include/freetype/internal/services/svtteng.h
		include/freetype/internal/services/svttglyf.h
		include/freetype/internal/services/svwinfnt.h
		include/freetype/internal/services/svxf86nm.h	
)

#devel folder
SET ( _DEVEL_
		devel/ft2build.h
		devel/ftoption.h
)
#src folder
SET ( _SRC_
		# src/autofit/afangles.c
		src/autofit/afangles.h
		# src/autofit/afcjk.c
		src/autofit/afcjk.h
		# src/autofit/afdummy.c
		src/autofit/afdummy.h
		src/autofit/aferrors.h
		# src/autofit/afglobal.c
		src/autofit/afglobal.h
		# src/autofit/afhints.c
		src/autofit/afhints.h
		# src/autofit/afindic.c
		src/autofit/afindic.h
		# src/autofit/aflatin.c
		src/autofit/aflatin.h
		# src/autofit/aflatin2.c
		src/autofit/aflatin2.h
		# src/autofit/afloader.c
		src/autofit/afloader.h
		# src/autofit/afmodule.c
		src/autofit/afmodule.h
		# src/autofit/afpic.c
		src/autofit/afpic.h
		src/autofit/aftypes.h
		# src/autofit/afwarp.c
		src/autofit/afwarp.h
		src/autofit/autofit.c
		
		# src/base/basepic.c
		src/base/basepic.h
		# src/base/ftadvanc.c
		# src/base/ftapi.c
		src/base/ftbase.c
		src/base/ftbase.h
		src/base/ftbbox.c
		# src/base/ftbdf.c
		src/base/ftbitmap.c
		# src/base/ftcalc.c
		src/base/ftcid.c
		# src/base/ftdbgmem.c
		# src/base/ftdebug.c
		src/base/ftfstype.c
		src/base/ftgasp.c
		# src/base/ftgloadr.c
		src/base/ftglyph.c
		# src/base/ftgxval.c
		src/base/ftinit.c
		# src/base/ftlcdfil.c
		# src/base/ftmac.c
		src/base/ftmm.c
		# src/base/ftobjs.c
		# src/base/ftotval.c
		# src/base/ftoutln.c
		# src/base/ftpatent.c
		src/base/ftpfr.c
		# src/base/ftpic.c
		# src/base/ftrfork.c
		# src/base/ftsnames.c
		# src/base/ftstream.c
		src/base/ftstroke.c
		src/base/ftsynth.c
		src/base/ftsystem.c
		# src/base/fttrigon.c
		src/base/fttype1.c
		# src/base/ftutil.c
		src/base/ftwinfnt.c
		# src/base/ftxf86.c
	
		src/bdf/bdf.c
		src/bdf/bdf.h
		# src/bdf/bdfdrivr.c
		src/bdf/bdfdrivr.h
		src/bdf/bdferror.h
		# src/bdf/bdflib.c
		
		src/bzip2/ftbzip2.c
		
		src/cache/ftcache.c
		# src/cache/ftcbasic.c
		# src/cache/ftccache.c
		src/cache/ftccache.h
		src/cache/ftccback.h
		# src/cache/ftccmap.c
		src/cache/ftcerror.h
		# src/cache/ftcglyph.c
		src/cache/ftcglyph.h
		# src/cache/ftcimage.c
		src/cache/ftcimage.h
		# src/cache/ftcmanag.c
		src/cache/ftcmanag.h
		# src/cache/ftcmru.c
		src/cache/ftcmru.h
		# src/cache/ftcsbits.c
		src/cache/ftcsbits.h

		src/cff/cff.c
		# src/cff/cffcmap.c
		src/cff/cffcmap.h
		# src/cff/cffdrivr.c
		src/cff/cffdrivr.h
		src/cff/cfferrs.h
		# src/cff/cffgload.c
		src/cff/cffgload.h
		# src/cff/cffload.c
		src/cff/cffload.h
		# src/cff/cffobjs.c
		src/cff/cffobjs.h
		# src/cff/cffparse.c
		src/cff/cffparse.h
		# src/cff/cffpic.c
		src/cff/cffpic.h
		src/cff/cfftoken.h
		src/cff/cfftypes.h		
		
		src/cid/ciderrs.h
		# src/cid/cidgload.c
		src/cid/cidgload.h
		# src/cid/cidload.c
		src/cid/cidload.h
		# src/cid/cidobjs.c
		src/cid/cidobjs.h
		# src/cid/cidparse.c
		src/cid/cidparse.h
		# src/cid/cidriver.c
		src/cid/cidriver.h
		src/cid/cidtoken.h
		src/cid/type1cid.c
		
		# src/gxvalid/gxvalid.c
		src/gxvalid/gxvalid.h
		# src/gxvalid/gxvbsln.c
		# src/gxvalid/gxvcommn.c
		src/gxvalid/gxvcommn.h
		src/gxvalid/gxverror.h
		# src/gxvalid/gxvfeat.c
		src/gxvalid/gxvfeat.h
		# src/gxvalid/gxvfgen.c
		# src/gxvalid/gxvjust.c
		# src/gxvalid/gxvkern.c
		# src/gxvalid/gxvlcar.c
		# src/gxvalid/gxvmod.c
		src/gxvalid/gxvmod.h
		# src/gxvalid/gxvmort.c
		src/gxvalid/gxvmort.h
		# src/gxvalid/gxvmort0.c
		# src/gxvalid/gxvmort1.c
		# src/gxvalid/gxvmort2.c
		# src/gxvalid/gxvmort4.c
		# src/gxvalid/gxvmort5.c
		# src/gxvalid/gxvmorx.c
		src/gxvalid/gxvmorx.h
		# src/gxvalid/gxvmorx0.c
		# src/gxvalid/gxvmorx1.c
		# src/gxvalid/gxvmorx2.c
		# src/gxvalid/gxvmorx4.c
		# src/gxvalid/gxvmorx5.c
		# src/gxvalid/gxvopbd.c
		# src/gxvalid/gxvprop.c
		# src/gxvalid/gxvtrak.c

		# src/gzip/adler32.c
		src/gzip/ftgzip.c
		# src/gzip/infblock.c
		src/gzip/infblock.h
		# src/gzip/infcodes.c
		src/gzip/infcodes.h
		src/gzip/inffixed.h
		# src/gzip/inflate.c
		# src/gzip/inftrees.c
		src/gzip/inftrees.h
		# src/gzip/infutil.c
		src/gzip/infutil.h
		src/gzip/zconf.h
		src/gzip/zlib.h
		# src/gzip/zutil.c
		src/gzip/zutil.h
		
		src/lzw/ftlzw.c
		# src/lzw/ftzopen.c
		src/lzw/ftzopen.h
	
		# src/otvalid/otvalid.c
		src/otvalid/otvalid.h
		# src/otvalid/otvbase.c
		# src/otvalid/otvcommn.c
		src/otvalid/otvcommn.h
		src/otvalid/otverror.h
		# src/otvalid/otvgdef.c
		# src/otvalid/otvgpos.c
		src/otvalid/otvgpos.h
		# src/otvalid/otvgsub.c
		# src/otvalid/otvjstf.c
		# src/otvalid/otvmath.c
		# src/otvalid/otvmod.c
		src/otvalid/otvmod.h	
		
		src/pcf/pcf.c
		src/pcf/pcf.h
		# src/pcf/pcfdrivr.c
		src/pcf/pcfdrivr.h
		src/pcf/pcferror.h
		# src/pcf/pcfread.c
		src/pcf/pcfread.h
		# src/pcf/pcfutil.c
		src/pcf/pcfutil.h
		
		src/pfr/pfr.c
		# src/pfr/pfrcmap.c
		src/pfr/pfrcmap.h
		# src/pfr/pfrdrivr.c
		src/pfr/pfrdrivr.h
		src/pfr/pfrerror.h
		# src/pfr/pfrgload.c
		src/pfr/pfrgload.h
		# src/pfr/pfrload.c
		src/pfr/pfrload.h
		# src/pfr/pfrobjs.c
		src/pfr/pfrobjs.h
		# src/pfr/pfrsbit.c
		src/pfr/pfrsbit.h
		src/pfr/pfrtypes.h
		
		# src/psaux/afmparse.c
		src/psaux/afmparse.h
		src/psaux/psaux.c
		src/psaux/psauxerr.h
		# src/psaux/psauxmod.c
		src/psaux/psauxmod.h
		# src/psaux/psconv.c
		src/psaux/psconv.h
		# src/psaux/psobjs.c
		src/psaux/psobjs.h
		# src/psaux/t1cmap.c
		src/psaux/t1cmap.h
		# src/psaux/t1decode.c
		src/psaux/t1decode.h
		
		# src/pshinter/pshalgo.c
		src/pshinter/pshalgo.h
		# src/pshinter/pshglob.c
		src/pshinter/pshglob.h
		src/pshinter/pshinter.c
		# src/pshinter/pshmod.c
		src/pshinter/pshmod.h
		src/pshinter/pshnterr.h
		# src/pshinter/pshpic.c
		src/pshinter/pshpic.h
		# src/pshinter/pshrec.c
		src/pshinter/pshrec.h
		
		src/psnames/psmodule.c
		src/psnames/psmodule.h
		src/psnames/psnamerr.h
		# src/psnames/psnames.c
		# src/psnames/pspic.c
		src/psnames/pspic.h
		src/psnames/pstables.h
		
		src/raster/ftmisc.h
		# src/raster/ftraster.c
		src/raster/ftraster.h
		# src/raster/ftrend1.c
		src/raster/ftrend1.h
		src/raster/raster.c
		src/raster/rasterrs.h
		# src/raster/rastpic.c
		src/raster/rastpic.h
		
		# src/sfnt/sfdriver.c
		src/sfnt/sfdriver.h
		src/sfnt/sferrors.h
		src/sfnt/sfnt.c
		# src/sfnt/sfntpic.c
		src/sfnt/sfntpic.h
		# src/sfnt/sfobjs.c
		src/sfnt/sfobjs.h
		# src/sfnt/ttbdf.c
		src/sfnt/ttbdf.h
		# src/sfnt/ttcmap.c
		src/sfnt/ttcmap.h
		src/sfnt/ttcmapc.h
		# src/sfnt/ttkern.c
		src/sfnt/ttkern.h
		# src/sfnt/ttload.c
		src/sfnt/ttload.h
		# src/sfnt/ttmtx.c
		src/sfnt/ttmtx.h
		# src/sfnt/ttpost.c
		src/sfnt/ttpost.h
		# src/sfnt/ttsbit.c
		src/sfnt/ttsbit.h
		# src/sfnt/ttsbit0.c
		
		# src/smooth/ftgrays.c
		src/smooth/ftgrays.h
		src/smooth/ftsmerrs.h
		# src/smooth/ftsmooth.c
		src/smooth/ftsmooth.h
		# src/smooth/ftspic.c
		src/smooth/ftspic.h
		src/smooth/smooth.c
		
		# src/tools/ftrandom/ftrandom.c
		# src/tools/apinames.c
		src/tools/chktrcmp.py
		src/tools/cordic.py
		src/tools/glnames.py
		src/tools/test_afm.c
		src/tools/test_bbox.c
		src/tools/test_trig.c
		
		src/truetype/truetype.c
		# src/truetype/ttdriver.c
		src/truetype/ttdriver.h
		src/truetype/tterrors.h
		# src/truetype/ttgload.c
		src/truetype/ttgload.h
		# src/truetype/ttgxvar.c
		src/truetype/ttgxvar.h
		# src/truetype/ttinterp.c
		src/truetype/ttinterp.h
		# src/truetype/ttobjs.c
		src/truetype/ttobjs.h
		# src/truetype/ttpic.c
		src/truetype/ttpic.h
		# src/truetype/ttpload.c
		src/truetype/ttpload.h
		
		# src/type1/t1afm.c
		src/type1/t1afm.h
		# src/type1/t1driver.c
		src/type1/t1driver.h
		src/type1/t1errors.h
		# src/type1/t1gload.c
		src/type1/t1gload.h
		# src/type1/t1load.c
		src/type1/t1load.h
		# src/type1/t1objs.c
		src/type1/t1objs.h
		# src/type1/t1parse.c
		src/type1/t1parse.h
		src/type1/t1tokens.h
		src/type1/type1.c
		
		# src/type42/t42drivr.c
		src/type42/t42drivr.h
		src/type42/t42error.h
		# src/type42/t42objs.c
		src/type42/t42objs.h
		# src/type42/t42parse.c
		src/type42/t42parse.h
		src/type42/t42types.h
		src/type42/type42.c
		
		src/winfonts/fnterrs.h
		src/winfonts/winfnt.c
		src/winfonts/winfnt.h
)

#include folder
SOURCE_GROUP("include" FILES
		${_INCLUDE_}
)
SOURCE_GROUP("include\\freetype" FILES
		${__FREETYPE_}
)
SOURCE_GROUP("include\\freetype\\config" FILES
		${___CONFIG_}
)
SOURCE_GROUP("include\\freetype\\internal" FILES
		${___INTERNAL}
)
SOURCE_GROUP("include\\freetype\\internal\\services" FILES
		${____SERVICES}
)

#devel folder
SOURCE_GROUP("devel" FILES
		${_DEVEL_}
)


#src folder
SOURCE_GROUP("src" FILES
		${_SRC_}
)

#<-------- Additional Include Directories ------------------>
INCLUDE_DIRECTORIES(
	#TODO:Make this clear and simple
	${CMAKE_SOURCE_DIR}/extlibs/freetype/include
	# should remove later
	#${CMAKE_SOURCE_DIR}/extlibs	
	#${CMAKE_SOURCE_DIR}/foundation
	
)

ADD_LIBRARY(
	FreeType 
	STATIC 
	${_INCLUDE_}
	${__FREETYPE_}
	${___CONFIG_}
	${___INTERNAL}
	${____SERVICES}
	${_DEVEL_}
	${_SRC_}	
 )
 ADD_DEFINITIONS(
	-DFT2_BUILD_LIBRARY
	 )
	
 #Organize projects into folders
SET_PROPERTY(TARGET FreeType PROPERTY FOLDER "1.Libs")

#SET ( CMAKE_C_FLAGS_DEBUG "/MTd")
#SET ( CMAKE_C_FLAGS_EDITOR_DEBUG "/MTd")
#SET ( CMAKE_C_FLAGS_EDITOR_RELEASE "/MT")
#SET ( CMAKE_C_FLAGS_RELEASE "/MT")

#SET ( CMAKE_C_FLAGS_PROFILE_DEBUG "/MTd")
#SET ( CMAKE_C_FLAGS_PROFILE_RELEASE "/MT")

 #_MACRO_COPY_T0_BINARY_DIR_AFTER_BUILD( FreeType .lib )