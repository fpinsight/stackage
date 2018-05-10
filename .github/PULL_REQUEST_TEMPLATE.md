Checklist:
- [ ] Meaningful commit message - please not `Update build-constraints.yml`
- [ ] At least 30 minutes have passed since Hackage upload
- [ ] On your own machine, in a new directory, you have successfully run the following set of commands (replace `$package` with the name of the package that is submitted, `$version` is the version of the package you want to get into Stackage):

      stack unpack $package-$version
      cd $package-$version
      stack init --resolver nightly
      stack build --resolver nightly --haddock --test --bench --no-run-benchmarks
