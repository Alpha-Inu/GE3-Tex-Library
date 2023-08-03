MDS Textures

The textures that appear on outfits and characters are saved in MDS format-an MDS file is a DDS file in disguise. These files are applied only to mdl files and they are compressed with DX10,
making some of them unreadable by GIMP. My personally recommended tool for editing these textures is paint.NET as it can read all the relevant formats/compression methods.
The way to edit these textures on your own is by changing the extension to .dds and loading them into any graphics program that can export DDS files, as long as it can also recompress/decompress
DX10-when saving your custom texture, always generate Mipmaps. I believe the correct method is BC3 (sRGB Dx10+), but everything from BC3 to BC7 seems to work also.

DirectDraw Surface (.DDS)[1024x1024,compressed: DX10,Mipmap]

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
 
	ALBEDO_TEX	              filename_A		-The texture you will see when an object is illuminated by the scene lighting
	SHADOW_TEX                    filename_S		-This texture will be visible on the object where a shadow is cast, 
	ARMH_TEX                      filename_ARMH
	NORMAL_TEX	              filename_N
	EMISSIVE_TEX                  filename_E
	RIM_TEX	                      filename_R

  	In the game, the dynamic lighting is achieved on character models by manipulating the opacity of the albedo texture in relation to 
   	wherever the light source is. 
