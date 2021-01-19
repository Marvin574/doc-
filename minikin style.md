The C++ style in Minikin follows Android Framework C++ Code Style Guide except for following rules:

Order of include
In dir/foo.cc or dir/foo_test.cc, whose main purpose is to implement or test the stuff in dir2/foo2.h, order your includes as follows:

dir2/foo.h
A blank line
C system files
C++ system files
A blank line
Other libraries' files
A blank line
Minikin public files
A blank line
Minikin private files
For example,

#include "minikin/Layout.h"  // The corresponding header file.

#include <math.h>  // C system header files.
#include <string>  // C++ system header files.

#include <hb.h>  // Other library, HarfBuzz, header file.
#include <log/log.h>  // Other library, Android, header file.
#include <unicode/ubidi.h>  // Other library, ICU, header file.

#include "minikin/Emoji.h"  // The minikin public header file.
#include "HbFontCache.h"  // The minikin private header file.
“<>” vs ""

#include <...> should be used for non local library files.
#include "..." should be used for minikin header files.
