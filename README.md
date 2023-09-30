# SiaNano

## Dependence
![](https://img.shields.io/badge/software-version-blue)  
[![](https://img.shields.io/badge/Guppy-v6.5.7-green)](https://community.nanoporetech.com/downloads)
[![](https://img.shields.io/badge/Minimap2-v2.24-green)](https://github.com/lh3/minimap2)
[![](https://img.shields.io/badge/samtools-v1.16.1-green)](https://github.com/samtools/samtools)  
[![](https://img.shields.io/badge/Epinano-v1.2.0-blue)](https://github.com/novoalab/EpiNano)
[![](https://img.shields.io/badge/Genome-hg38-orange)](https://hgdownload.soe.ucsc.edu/goldenPath/hg38/bigZips/)


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#Intallation">Intallation</a>
    </li>
    <li><a href="#Usage">Usage</a></li>
    <li><a href="#References">References</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#Contact">Contact</a></li>
  </ol>
</details>

## Intallation
1.Install environment: check the env directory of yml files
   ```sh
   conda env create -f $environment.yml
   ```
2.prepare tookit: check and modify the tookit.py file.
    
## Usage
1.Minimap
   ```sh
   conda activate mDRS
   python 02.minimap.py -i $fastq -o $out -r $fasta
   ```
2.Extract base-calling error features
   ```sh
   python 02.Epinano_Variants.py -R $ref -b $bam -s $sam2tsv -n 16 -T t
   ```
3.Slide features
   ```sh
   python 09.Epinano_slide_feature.py $per.site.csv 5
   ```

## License
Distributed under the GPL-2.0 License License. See LICENSE for more information.

## Contact
liuchw3@mail2.sysu.edu.cn

## Reference
