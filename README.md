# Lab 06 - B222270044 - Г. Оргилсайхан

**Сэдэв:** Тест тохиолдол боловсруулах — Category-Partition ба PICT (F.CSA313, 2026)

```
$ cat results/pict-build.txt
pict commit ab76c25 2026-09-08
Pairwise Independent Combinatorial Testing

Usage: pict model [options]
```

Орчин: Ubuntu 26.04.1 LTS · cmake 4.2.3 · g++ 15.2.0 · PICT (эх кодоос, commit `ab76c25`)

## Алхам 1: PICT-ийг эх кодоос бүтээх

PICT-ийн эх кодыг лабын репоосоо **гадна** `~/tools/pict`-д clone хийж cmake-ээр бүтээсэн:

```bash
mkdir -p ~/tools && cd ~/tools && git clone https://github.com/microsoft/pict && cd pict
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build -j4
cp build/cli/pict ~/.local/bin/     # sudo эрхгүй тул /usr/local/bin биш ~/.local/bin (PATH-д байгаа)
```

Нотолгоо `results/pict-build.txt`-д (`git -C ~/tools/pict log -1 ...; pict | head -3`). `.gitignore`-д `pict/`, `build/` нэмсэн тул PICT-ийн эх код, build хавтас репод орохгүй.
