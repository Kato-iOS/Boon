# Boon: Swift Library for Ethereum Interaction

"Boon, your compact powerhouse for Web3 in SwiftUI. Tailored for Swift, this tool is a gateway to seamless decentralized web interactions. Crafted for ease, it features the best documentation around. Boon isn't just a library, it's your trusted guide to the Web3 universe with SwiftUI. Embrace the future, swiftly."

Boon is a Swift library designed for signing transactions and interacting with Smart Contracts on the Ethereum Network.

This library empowers you to connect to an Ethereum node such as geth to send transactions and read values from Smart Contracts, eliminating the need to write your own implementations of these protocols.

Boon supports iOS, macOS, tvOS, watchOS.

Why Boon? Here's The Boon Difference!
Boon has been engineered from the ground up to become your go-to toolkit for your Ethereum ventures. But what makes it stand out in the crowd? Well, we'd like you to meet the four superheroes of Boon - Modularity, Portability, Speed, and Efficiency.

Modularity, the Shape-Shifter
Modularity in Boon is not just a concept, it's our ethos. With Boon, you get to command your own Superhero toolkit. Need just the essentials? The basic Boon package via Swift Package Manager (SPM) has got you covered with fundamental operations such as transaction signing and interacting with an HTTP RPC server.

Craving for some advanced power? Just call on additional sidekicks! IPC RPC support, PromiseKit extensions, JSON ABIs parsing for Ethereum Smart Contracts are all just a Swift command away. And if you are yearning for something even more specific, worry not! Our APIs are open-ended, ready for you to expand, tweak and tune as per your unique needs.

The upshot? Boon is more than just a tool. It's a flexible, customizable partner-in-crime for all your Ethereum adventures.

Portability, the Multiverse Traveller
Like the superhero that can be in multiple places at once, Portability lets Boon be available everywhere. Conceived with a dream to seamlessly integrate with Swift Package Manager across platforms, Boon today struts its stuff on iOS, macOS, tvOS, watchOS, and Linux. No matter where your development journey takes you, Boon is always by your side.

Speed and Efficiency, the Time Lords
When you are out there, building the future of decentralized applications, every tick of the clock counts. Enter Speed and Efficiency, the twin Time Lords of Boon.

Speed ensures Boon's responses are as swift as a superhero's reflexes. On the other hand, Efficiency guarantees that you get the maximum performance with minimal overhead. And the result? A streamlined development workflow where you focus on crafting awesome DApps, while Boon handles the nitty-gritty of Ethereum interactions.

But that's not all. Just like Time Lords, our APIs are thread-safe and built to thrive in highly concurrent environments, ensuring you get optimal performance, all the time, every time.

The Boon Difference - Unleashing Your Inner Superhero
These four superheroes form the essence of the Boon Difference - a toolkit designed to let you channel your inner superhero, empowering you to create, innovate, and revolutionize the Ethereum ecosystem. So why wait? Unleash your powers with Boon and redefine the future of Ethereum!

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
