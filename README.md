# PNG-Parser

## Description
A .png file parser in C.

## Requirements

* Import and include SDL.h header from [SDL](https://www.libsdl.org/) library v.2.0 or higher. Only works correctly with 
* Only 8 bit truecolor with alpha supported. In other words, a typical RGBA image where each channel is one byte.
* Interlacing not supported.

## Functions
| **Name** | **Params**| **Return** | **Description** |
|----------|-----------|------------|-----------------|
| **png_open_file** | *file_path*: relative path of the file to open. <br/><br/> *file_size*: size of the file content datas. | A uint8 pointer to content data. | On first call fills *file_size* pointer with informations about memory to be allocated. On second call returns the pointer to allocated memory with file data. |
| **png_parse** | *file_data*: pointer to data content of a bitmap file. <br/><br/> *texture_width*: where to store texture width infos. <br/><br/> *texture_height*: where to store texture height infos. | A uint8 pointer to texture pixels parsed data. | Parse raw bitmap datas into texture pixels data to use on *SDL_Texture* function or other graphic libraries. |

**Find an example .png image on *Example* directory.**
