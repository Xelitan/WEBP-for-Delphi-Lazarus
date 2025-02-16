# WEBP-for-Delphi-Lazarus
Read &amp; write WEBP images in Delphi, Free Pascal and Lazarus 
Requires .DLL files (included). For Linux and MacOS you need to download binaries from libflif project.

## Usage examples

### Using TImage / TPicture

    Image1.Picture.LoadFromFile('test.webp');

### Using classes directly

    var w: TWebpImage;
    begin
      w := TWebpImage.Create;
      w.Assign(Bitmap...);
      w.SaveToFile('test.webp');
      w.free;
    end;

# Tested under 64 bit Lazarus and 64 bit Delphi 12.

Should work under other 64 bit Delphis.
Needs tests under 32 bit Lazarus and 32 bit Delphi.

## Linux (Debian, Ubuntu, Mint)

1) apt install apt-file libwebp-dev
2) apt-file search libwebp.so
It will list you how your libwebp.so files are named *exactly* and where they are
3) Open WebpImage.pas and edit "const LIBWEBPF"
4) Change the value of that const. Enter filename (excluding path) found in step 2
5) Compile and run
