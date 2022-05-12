# BioJulia Docker Image

[![Build Docker](https://github.com/MillironX/docker-BioJulia/actions/workflows/build_docker.yml/badge.svg)](https://github.com/MillironX/docker-BioJulia/actions/workflows/build_docker.yml)
[![Unlicense](https://img.shields.io/github/license/MillironX/docker-BioJulia)](https://github.com/MillironX/docker-BioJulia/blob/master/LICENSE)
[![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/MillironX/docker-BioJulia)](https://github.com/MillironX/docker-BioJulia/tags)
[![Docker Pulls](https://img.shields.io/docker/pulls/millironx/biojulia)](https://hub.docker.com/r/millironx/biojulia)
[![Docker Repository on Quay](https://quay.io/repository/millironx/biojulia/status "Docker Repository on Quay")](https://quay.io/repository/millironx/biojulia)

Most of the [BioJulia] ecosystem made available as a single ready-made [Docker]
image. Built on top of my [JuliaPro image].

Note: the version of the image refers to the latest version of BioSequences that
will resolve in the Pkg environment.

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

Everything from my [JuliaPro image], minus

- [ ] ~~[Flux](https://github.com/FluxML/Flux.jl)~~
- [ ] ~~[Metalhead](https://github.com/FluxML/Metalhead.jl)~~
- [ ] ~~[Knet](https://github.com/denizyuret/Knet.jl)~~

plus

### Programming Libraries

- [x] [Automa](https://github.com/BioJulia/Automa.jl)
- [x] [BioGenerics](https://github.com/BioJulia/BioGenerics.jl)
- [ ] ~~[BioTools](https://github.com/BioJulia/BioTools.jl)~~ (Dependent on
  BioSequnces v1. Seriously?)
- [x] [PopGenCore](https://github.com/BioJulia/PopGenCore.jl)

### Biological Types

- [x] [BioAlignments](https://github.com/MillironX/BioAlignments.jl)
- [x] [BioSequences](https://github.com/BioJulia/BioSequences.jl)
- [x] [BioStructures](https://github.com/BioJulia/BioStructures.jl)
- [x] [BioSymbols](https://github.com/BioJulia/BioSymbols.jl)
- [x] [GenomeGraphs](https://github.com/BioJulia/GenomeGraphs.jl)
- [x] [IntervalTrees](https://github.com/BioJulia/IntervalTrees.jl)
- [x] [SubstitutionModels](https://github.com/BioJulia/SubstitutionModels.jl)

### File Formats

- [x] [BED](https://github.com/BioJulia/BED.jl)
- [ ] ~~[BigBed](https://github.com/BioJulia/BigBed.jl)~~ (Dependency mismatch
  with PopGen)
- [x] [BigWig](https://github.com/BioJulia/BigWig.jl)
- [x] [FASTX](https://github.com/BioJulia/FASTX.jl)
- [x] [GenomicAnnotations](https://github.com/BioJulia/GenomicAnnotations.jl)
- [x] [GenomicFeatures](https://github.com/BioJulia/GenomicFeatures.jl)
- [x] [MMTF](https://github.com/BioJulia/MMTF.jl)
- [x] [TwoBit](https://github.com/BioJulia/TwoBit.jl)
- [x] [VariantCallFormat](https://github.com/rasmushenningsson/VariantCallFormat.jl)
- [x] [XAM](https://github.com/MillironX/XAM.jl)

### Analyses

- [x] [KmerAnalysis](https://github.com/BioJulia/KmerAnalysis.jl)
- [x] [PopGen](https://github.com/BioJulia/PopGen.jl.git)

### Compression Codecs and File Processing

- [x] [BGZFStreams](https://github.com/BioJulia/BGZFStreams.jl)
- [x] [CodecBase](https://github.com/bicycle1885/CodecBase.jl)
- [x] [CodecBzip2](https://github.com/bicycle1885/CodecBzip2.jl)
- [x] [CodecLz4](https://github.com/invenia/CodecLz4.jl)
- [x] [CodecXz](https://github.com/bicycle1885/CodecXz.jl)
- [x] [CodecZlib](https://github.com/bicycle1885/CodecZlib.jl)
- [x] [CodecZstd](https://github.com/bicycle1885/CodecZstd.jl)
- [x] [Indexes](https://github.com/BioJulia/Indexes.jl)
- [x] [TranscodingStreams](https://github.com/JuliaIO/TranscodingStreams.jl)

### Data Storage and Retrieval

- [x] [BioServices](https://github.com/BioJulia/BioServices.jl)
- [x] [ReadDatastores](https://github.com/BioJulia/ReadDatastores.jl)

[`JULIA_DEPOT_PATH`]: https://docs.julialang.org/en/v1/manual/environment-variables/#JULIA_DEPOT_PATH
[biojulia]: https://biojulia.net
[docker hub]: https://hub.docker.com
[docker]: https://www.docker.com
[github container registry]: https://ghcr.io
[juliapro image]: https://github.com/MillironX/docker-JuliaPro
[podman]: https://podman.io
[quay]: https://quay.io
[singularity/apptainer]: https://apptainer.org
