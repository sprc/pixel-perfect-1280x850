# xrandr-nofilter
I'm doing this to (arguably) improve my remote desktop experience on a Chromebook Pixel. My destination Windows machine can't handle HiDPI gracefully and the bilinear filter is just a little too fuzzy for my taste.

I'm assuming you're on Ubuntu Trusty. If you're not, well, you're pretty clever, aren't you? You figure it out.

First, some prereqs:
	sudo apt-get install build-essential autoconf xutils-dev libxrandr-dev-lts-trusty

Then:
	git clone https://github.com/sprc/xrandr-nofilter.git
	cd xrandr-nofilter
	sh autogen.sh
	make

To use:
	./xrandr --output eDP1 --auto --scale 0.5x0.5

...replacing ./ with the path to your custom xrandr. If you don't put a path in, you'll just be executing your plain old stock xrandr, so this is important!

