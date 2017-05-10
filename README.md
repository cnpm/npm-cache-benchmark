# npm vs shrinkpack vs npm5 vs yarn vs npminstall

Benchmarks of [npm][1], [npm5][2], [shrinkpack][3], [yarn][4] and [npminstall][5] install times.

## Results

### Travis CI Ubuntu

| Installer | Average over 5 runs |
|:--|--:|
| npminstall 3.x (cached) | 9.13s |
| npminstall 3.x | 9.32s |
| npm 5.x (shrinkpacked, compressed) | 10.50s |
| npm 5.x | 12.46s |
| yarn --offline | 13.39s |
| yarn | 14.31s |
| npm 5.x (cached) | 14.38s |
| npm 4.x (cached) | 15.83s |
| npm 4.x | 16.32s |
| npm 4.x (shrinkpacked) | 19.85s |
| npm 4.x (shrinkpacked, compressed) | 20.25s |

## Running the Benchmarks

### Locally

```bash
git clone https://github.com/cnpm/npm-cache-benchmark.git
cd npm-cache-benchmark
npm install
npm start
```

## Full Results

### Travis CI Ubuntu

https://travis-ci.org/cnpm/npm-cache-benchmark/jobs/230666504#L769

```
$ npm start

Run 1
npm 4.x: 15.35s (average 15.35s)
npm 4.x (cached): 15.92s (average 15.92s)
npm 4.x (shrinkpacked): 18.90s (average 18.90s)
npm 4.x (shrinkpacked, compressed): 19.92s (average 19.92s)
yarn: 15.23s (average 15.23s)
yarn --offline: 14.07s (average 14.07s)
npm 5.x: 12.25s (average 12.25s)
npm 5.x (cached): 20.80s (average 20.80s)
npm 5.x (shrinkpacked, compressed): 11.77s (average 11.77s)
npminstall 3.x: 8.47s (average 8.47s)
npminstall 3.x (cached): 9.03s (average 9.03s)

Run 2
npm 4.x: 15.83s (average 15.59s)
npm 4.x (cached): 15.63s (average 15.77s)
npm 4.x (shrinkpacked): 19.55s (average 19.22s)
npm 4.x (shrinkpacked, compressed): 19.64s (average 19.78s)
yarn: 13.54s (average 14.38s)
yarn --offline: 12.79s (average 13.43s)
npm 5.x: 11.94s (average 12.09s)
npm 5.x (cached): 11.80s (average 16.30s)
npm 5.x (shrinkpacked, compressed): 10.03s (average 10.90s)
npminstall 3.x: 8.46s (average 8.47s)
npminstall 3.x (cached): 8.10s (average 8.57s)

Run 3
npm 4.x: 14.83s (average 15.34s)
npm 4.x (cached): 15.40s (average 15.65s)
npm 4.x (shrinkpacked): 18.85s (average 19.10s)
npm 4.x (shrinkpacked, compressed): 19.95s (average 19.84s)
yarn: 14.12s (average 14.29s)
yarn --offline: 13.72s (average 13.53s)
npm 5.x: 12.09s (average 12.09s)
npm 5.x (cached): 13.66s (average 15.42s)
npm 5.x (shrinkpacked, compressed): 10.84s (average 10.88s)
npminstall 3.x: 10.10s (average 9.01s)
npminstall 3.x (cached): 9.15s (average 8.76s)

Run 4
npm 4.x: 20.20s (average 16.55s)
npm 4.x (cached): 17.04s (average 16.00s)
npm 4.x (shrinkpacked): 21.10s (average 19.60s)
npm 4.x (shrinkpacked, compressed): 21.75s (average 20.32s)
yarn: 14.23s (average 14.28s)
yarn --offline: 13.69s (average 13.57s)
npm 5.x: 14.70s (average 12.74s)
npm 5.x (cached): 14.61s (average 15.22s)
npm 5.x (shrinkpacked, compressed): 10.12s (average 10.69s)
npminstall 3.x: 9.05s (average 9.02s)
npminstall 3.x (cached): 9.32s (average 8.90s)

Run 5
npm 4.x: 15.38s (average 16.32s)
npm 4.x (cached): 15.15s (average 15.83s)
npm 4.x (shrinkpacked): 20.87s (average 19.85s)
npm 4.x (shrinkpacked, compressed): 20.00s (average 20.25s)
yarn: 14.43s (average 14.31s)
yarn --offline: 12.68s (average 13.39s)
npm 5.x: 11.32s (average 12.46s)
npm 5.x (cached): 11.03s (average 14.38s)
npm 5.x (shrinkpacked, compressed): 9.75s (average 10.50s)
npminstall 3.x: 10.50s (average 9.32s)
npminstall 3.x (cached): 10.04s (average 9.13s)
```

<!-- links -->
[1]: https://www.npmjs.com
[2]: https://www.npmjs.com/package/npm5
[3]: https://github.com/JamieMason/shrinkpack
[4]: https://github.com/yarnpkg/yarn
[5]: https://github.com/cnpm/npminstall
