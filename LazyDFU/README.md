# Lazy DataFixerUpper

Makes Minecraft 1.13+ jarmods launch **a lot** faster. Just try it, it can improve start times by a lot. 
Adaptation of [LazyDFU](https://github.com/astei/lazydfu) for jarmods. You might need to change some class and method 
names cuz I wrote this in 1.16.5 using mojang mappings.

## How do I use this thing?

Add [this file](https://github.com/TheOddGarlic/MCPSnippets/blob/master/LazyDFU/LazyDataFixerBuilder.java) to your project. 
Don't forget to update package names. In net.minecraft.util.datafix.DataFixesManager replace 
`DataFixerBuilder datafixerbuilder = new DataFixerBuilder(SharedConstants.getCurrentVersion().getWorldVersion());`
with `DataFixerBuilder datafixerbuilder = new LazyDataFixerBuilder(SharedConstants.getCurrentVersion().getWorldVersion());` and see the magic happen.
