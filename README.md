# A collection of my texture replacements for GOD EATER 3 if/when I make them.
Unpacking guide found on God Eater 3 Modding Community Discord.


DDS Textures

Many of the UI, menu and special event icons for the game use the industry standard DDS files and 
can be opened in GIMP or Microsoft Visual Studio but some are compressed with DX10 and would
require a more aggressive tool such as paint.NET. 

I primarily use paint.NET for this task as GIMP's DDS plugin is severely outdated. Most of the 
textures you will find here I have recompressed with BC6/7. paint.NET is the only tool I know of 
that is able to do this.

Place .dds files in "\resource\target\win\texture"

MDS Textures

The textures that appear on outfits and characters are saved in MDS format-MDS files are some
kind of dds texture file with a different extension. These files are applied only to mdl files,
These mds texture files can be manipulated by changing the extension to .dds and the standards of dds 
still apply. Some MDS files are compressed with a newer method that GIMP's DDS plugin cannot load.
These files can be edited via Microsoft Visual Studio.

Place .mds files in "\resource\target\win\mdltex"

Files with the .mds extension are named as such

	Filename                                Example
	
	P_B_MA0311_03_S.mds		       1_2_3a3b4_5.dds	

	1  - Entity name 		 - "player"	                        	"entity" refers to a character, monster, or prop.
	2  - Entity part		 - "bottom"		              	 	"part" refers to a limb or section.
	3a - Gender 			 - "male" 		              	        gender specific descriptor code.
	3b - Code			 - "0311"			                database descriptor used to match an mds to mdl.
	4  - Variation   	         - "03"				                outfits come in sets, this defines which is which.
	5  - Class	 		 - "S"				                  outlines texture type [shadow,albedo,etc.]
	
	This texture is for the "Shadow" texture of Variation 3 of the Blaze Walker outfit set, the 
	Forest Walker lower body costume on the male player character
	
	*Understand that entity, prop, code, variation, and class are not game-defined terms and 
	were chosen to make the abstraction easier to visualize
	
	Texture types:                Example
 
	ALBEDO_TEX	              filename_A
	SHADOW_TEX                    filename_S
	ARMH_TEX                      filename_ARMH
	NORMAL_TEX	              filename_N
	EMISSIVE_TEX                  filename_E
	RIM_TEX	                      filename_R
