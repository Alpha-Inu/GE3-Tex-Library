# A collection of my texture replacements for GOD EATER 3 if/when I make them. Unpacking guide 
not included.

DIY General Information


DDS Textures

Many of the UI and menu icons for the game you will find in DDS format and can be edited with
GIMP or Microsoft Visual Studio.

MDS Textures

The textures that appear on outfits and characters are saved in MDS format

MDS files are some kind of dds texture file with a different extension. These files are applied 
only to mdl files, whearas ui element textures use the industry standard dds files. These mds 
texture files can be manipulated by changing the extension to .dds and the standards of dds 
still apply. Some MDS files are compressed with a newer method that GIMP's DDS plugin cannot load.
These files can be edited via Microsoft Visual Studio.

Files with the .mds extension are named as such

	Filename                                Example
	
	P_B_MA0311_03_S.mds		       1_2_3a3b4_5.dds	

	1  - Entity name 		 - "player"	                        	"entity" refers to a character, monster, or prop.
	2  - Entity part		 - "bottom"		              	 	"part" refers to a limb or section.
	3a - Gender 			 - "male" 		              	        gender specific descriptor code.
	3b - Code			 - "0311"			                database descriptor used to match an mds to mdl.
	4  - Variation   	         - "03"				                outfits come in sets, this defines which is which.
	5  - Class	 		 - "S"				                  outlines texture type [shadow,albedo,etc.]
	
	This texture is for the "Shadow" texture of Variation 3 of the Frost Walker outfit set, the 
	Forest Walker lower body costume on the male player character
	
	*Understand that entity, prop, code, variation, and class are not game-defined terms and 
	were chosen to make the abstraction easier to visualize
	
	Texture types:                Example
 
	ALBEDO_	                      filename_A
	SHADOW_TEX                    filename_S
	ARMH_TEX                      filename_ARMH
	NORMAL_TEX	              filename_N
	EMISSIVE_TEX                  filename_E
	RIM_TEX	                      filename_R
