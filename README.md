SimpleOrderbook is an interactive back-end for handling and matching real-time financial market order flow. It's currently in early development, has undergone almost no testing, and is currently only intended for animating market models and simulations.

The core module is implemented as a C++ class, providing a low-level interface. The Python-C API extension module sits on top - wrapping the object - providing its own object-oriented interface.

#####++ Features 
- market, limit, stop-market, and stop-limit orders that trigger callbacks when executed
- cancel/replace orders by ID
- query market state(bid size, volume etc.), dump orders to stdout, view Time & Sales 
- MarketMaker objects that operate 'inside' the Orderbook (in progress)
- customizable market parameters( increment size, # of market makers etc.)
- (possibly) more advanced order types

#####++ Requirements
- C++ or Python  
- c++11(c++0x) compiler support (or a willingness to backport)
- knowledge of basic market order types, terminology, concepts etc.

#####++ Files
- simple_orderbook.hpp:  the (only) header for both modules
- simple_orderbook.cpp:  the pure C++ module in namespace NativeLayer
- python/simpleorderbook.cpp:  the Python-C API extension module that sits on top of simple_orderbook.cpp
- python/setup.py:  the python setup script that builds/installs the extension module (you'll probably have to change the py_... variables to match your own system; see python docs)

#####++ Licensing & Warranty

*SimpleOrderbook is released under the GNU General Public License(GPL); a copy (LICENSE.txt) should be included. If not, see http://www.gnu.org/licenses. The author reserves the right to issue current and/or future versions of SimpleOrderbook under other licensing agreements. Any party that wishes to use SimpleOrderbook, in whole or in part, in any way not explicitly stipulated by the GPL, is thereby required to obtain a separate license from the author. The author reserves all other rights.*

*This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details. 