# Keccak256-collisions

This repository includes rainbow tables that using the Keccak256 hash algorithm to generate common English words.

No salt was added when computing the hashes, allowing one to look up a specified word's hash. This is concerning since Keccak256 is widely used in Ethereum applications.This helps to demonstrate some of the security vulnerabilities of using Keccak256 in Ethereum and blockchain and can serve as an example for studying hash algorithms and cryptography.

The English words dataset from  the [words.txt](https://raw.githubusercontent.com/dwyl/english-words/master/words.txt) file in the [english-words](https://github.com/dwyl/english-words) repository was used,  over 466k English word hashes were calculated.

----

A word example:

```
import (
	"encoding/hex"
	"fmt"
  
	"github.com/ethereum/go-ethereum/crypto"
)

func ExampleKeccak256Hash() {
	wordsHash := crypto.Keccak256Hash([]byte("example")).String()
	// No '0x' prefix
	fmt.Println(wordsHash[2:])
	//Output: 6fd43e7cffc31bb581d7421c8698e29aa2bd8e7186a394b85299908b4eb9b175
}

```

## Usage

```bash

```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

## License

[CC0 1.0 Universal](LICENSE)

## Acknowledgments

* [english-words](https://github.com/dwyl/english-words)
