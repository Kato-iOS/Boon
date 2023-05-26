# Boon: Swift Library for Ethereum Interaction

"Boon, your compact powerhouse for Web3 in SwiftUI. Tailored for Swift, this tool is a gateway to seamless decentralized web interactions. Crafted for ease, it features the best documentation around. Boon isn't just a library, it's your trusted guide to the Web3 universe with SwiftUI. Embrace the future, swiftly."

Boon is a Swift library designed for signing transactions and interacting with Smart Contracts on the Ethereum Network.

This library empowers you to connect to an Ethereum node such as geth or erigon (like Chainnodes) to send transactions and read values from Smart Contracts, eliminating the need to write your own implementations of these protocols.

Boon supports iOS, macOS, tvOS, watchOS, and Linux using Swift Package Manager.

Example
For example usage, refer to the repository's tests.

Why Boon?
While there are some other libraries similar to Boon written in Swift, they might not cater to your specific use-cases due to their limitations.

Boon was created keeping in mind modularity, portability, speed, and efficiency.

Let's take a deeper look into what this means:

Modularity
Boon has been designed with modularity in mind. By installing or using the basic Boon Swift Package Manager (SPM) product, you can access the most fundamental functions such as transaction signing and interacting with an HTTP RPC server.

Should you want to add support for IPC RPC or anything else, you can simply create a library that depends on Boon and implements the desired functionality. If you wish to use PromiseKit extensions for Boon calls, you can either use the provided PromiseKit SPM product or create your own. To conveniently parse JSON ABIs for Ethereum Smart Contracts, use the provided ABI Parsing SPM product.

Moreover, if you want to add functionality to Boon not yet provided, you don't have to wait until it gets merged and released in a version bump. You can simply extend or update functionality within your own app as our APIs are open for changes.

This makes Boon a flexible and customizable tool for your Ethereum interactions.

Portability
Boon was started with the aim of being used with Swift Package Manager across different platforms. Thus, Boon is available through Swift Package Manager on iOS, macOS, tvOS, watchOS, and Linux.

Speed and Efficiency
We have aimed to create Boon as a fast and efficient library that streamlines your development workflow, enabling you to focus on building great DAPPS without worrying about the implementation details.

Our APIs are thread-safe and designed for use in highly concurrent applications.

Installation
Boon is compatible with Swift Package Manager v5 (Swift 5 and above). Simply add it to the dependencies in your Package.swift.

swift
Copy code
dependencies: [
    .package(url: "https://github.com/your-github/Boon.git", from: "0.6.0")
]
Then add it to your target dependencies:

swift
Copy code
targets: [
    .target(
        name: "MyProject",
        dependencies: [
            .product(name: "Boon", package: "Boon"),
            .product(name: "BoonPromiseKit", package: "Boon"),
            .product(name: "BoonContractABI", package: "Boon"),
        ]
    ),
    .testTarget(
        name: "MyProjectTests",
        dependencies: ["MyProject"])
]
Note: BoonPromiseKit and BoonContractABI are optional and you only have to put them into your target dependencies if you wish to use them.

After the installation, you can import Boon in your Swift files.

swift
Copy code
import Boon

// Optional
import BoonPromiseKit
import BoonContractABI
Usage
With Boon, you can leverage an Ethereum node on a server to communicate with Ethereum. You can send signed transactions, read contract data, call contract functions, and much more.

For more detailed usage examples, refer to the official repository's documentation and test cases.
