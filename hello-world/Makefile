.PHONY: default
default:
	@echo "Building for macOS ARM64..."
	$(MAKE) HelloWorld_macos

HelloWorld_macos: HelloWorld_macos.o
	ld -o HelloWorld_macos HelloWorld_macos.o -lSystem -syslibroot `xcrun -sdk macosx --show-sdk-path` -e _start -arch arm64

HelloWorld_macos.o: HelloWorld_macos.s
	as -arch arm64 -o HelloWorld_macos.o HelloWorld_macos.s

.PHONY: clean
clean:
	@echo "Removing files for macOS ARM64..."
	rm -f HelloWorld_macos HelloWorld_macos.o
