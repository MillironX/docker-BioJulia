# BioJulia Docker Image

[![Build Docker](https://github.com/MillironX/docker-BioJulia/actions/workflows/build.yml/badge.svg)](https://github.com/MillironX/docker-BioJulia/actions/workflows/build.yml)
[![Unlicense](https://img.shields.io/github/license/MillironX/docker-BioJulia)](https://github.com/MillironX/docker-BioJulia/blob/master/LICENSE)
[![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/MillironX/docker-BioJulia)](https://github.com/MillironX/docker-BioJulia/tags)
[![Docker Pulls](https://img.shields.io/docker/pulls/millironx/biojulia)](https://hub.docker.com/r/millironx/biojulia)
[![Docker Repository on Quay](https://quay.io/repository/millironx/biojulia/status "Docker Repository on Quay")](https://quay.io/repository/millironx/biojulia)

Most of the [BioJulia] ecosystem made available as a single ready-made [Docker]
image. Built on top of my [JuliaPro image].

## Usage

The image is hosted on [Docker Hub], [Quay], and the [GitHub Container
Registry], and is compatible with [Docker], [Podman], and
[Singularity/Apptainer], and probably others.

```bash
docker pull millironx/biojulia:latest
podman pull quay.io/millironx/biojulia:latest
singularity pull docker://ghcr.io/millironx/biojulia:latest
```

The packages are installed in a depot in `/usr/local/share/julia`, so keep this
in mind when overwriting the [`JULIA_DEPOT_PATH`] variable. For more information
on the rationale for this and examples, see

- nf-core tools discussion: <https://github.com/nf-core/tools/pull/1317>
- Alex Peltzer's blog: <https://apeltzer.github.io/post/03-julia-lang-nextflow>

## Included Packages

Everything from my [JuliaPro image], plus

### Programming Libraries

- [ ] [Automa](https://github.com/BioJulia/Automa.jl)
- [ ] [BioGenerics](https://github.com/BioJulia/BioGenerics.jl)
- [ ] [BioTools](https://github.com/BioJulia/BioTools.jl)
- [ ] [PopGenCore](https://github.com/BioJulia/PopGenCore.jl)

### Biological Types

- [ ] [BioAlignments](https://github.com/MillironX/BioAlignments.jl)
- [ ] [BioSequences](https://github.com/BioJulia/BioSequences.jl)
- [ ] [BioStructures](https://github.com/BioJulia/BioStructures.jl)
- [ ] [BioSymbols](https://github.com/BioJulia/BioSymbols.jl)
- [ ] [GenomeGraphs](https://github.com/BioJulia/GenomeGraphs.jl)
- [ ] [IntervalTrees](https://github.com/BioJulia/IntervalTrees.jl)
- [ ] [SubstitutionModels](https://github.com/BioJulia/SubstitutionModels.jl)

### File Formats

- [ ] [BED](https://github.com/BioJulia/BED.jl)
- [ ] [BigBed](https://github.com/BioJulia/BigBed.jl)
- [ ] [BigWig](https://github.com/BioJulia/BigWig.jl)
- [ ] [FASTX](https://github.com/BioJulia/FASTX.jl)
- [ ] [GenomicAnnotations](https://github.com/BioJulia/GenomicAnnotations.jl)
- [ ] [GenomicFeatures](https://github.com/BioJulia/GenomicFeatures.jl)
- [ ] [MMTF](https://github.com/BioJulia/MMTF.jl)
- [ ] [TwoBit](https://github.com/BioJulia/TwoBit.jl)
- [ ] [VariantCallFormat](https://github.com/rasmushenningsson/VariantCallFormat.jl)
- [ ] [XAM](https://github.com/MillironX/XAM.jl)

### Analyses

- [ ] [KmerAnalysis](https://github.com/BioJulia/KmerAnalysis.jl)
- [ ] [PopGen](https://github.com/BioJulia/PopGen.jl.git)

### Compression Codecs and File Processing

- [ ] [BGZFStreams](https://github.com/BioJulia/BGZFStreams.jl)
- [ ] [CodecBase](https://github.com/bicycle1885/CodecBase.jl)
- [ ] [CodecBzip2](https://github.com/bicycle1885/CodecBzip2.jl)
- [ ] [CodecLz4](https://github.com/invenia/CodecLz4.jl)
- [ ] [CodecXz](https://github.com/bicycle1885/CodecXz.jl)
- [ ] [CodecZlib](https://github.com/bicycle1885/CodecZlib.jl)
- [ ] [CodecZstd](https://github.com/bicycle1885/CodecZstd.jl)
- [ ] [Indexes](https://github.com/BioJulia/Indexes.jl)
- [ ] [TranscodingStreams](https://github.com/JuliaIO/TranscodingStreams.jl)

### Data Storage and Retrieval

- [ ] [BioServices](https://github.com/BioJulia/BioServices.jl)
- [ ] [ReadDatastores](https://github.com/BioJulia/ReadDatastores.jl)

[`JULIA_DEPOT_PATH`]: https://docs.julialang.org/en/v1/manual/environment-variables/#JULIA_DEPOT_PATH
[biojulia]: https://biojulia.net
[docker hub]: https://hub.docker.com
[docker]: https://www.docker.com
[github container registry]: https://ghcr.io
[juliapro image]: https://github.com/MillironX/docker-JuliaPro
[podman]: https://podman.io
[quay]: https://quay.io
[singularity/apptainer]: https://apptainer.org
