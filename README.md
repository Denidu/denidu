### Hi there 👋

<pre>

import SwiftUI

struct DeniduView: View {

    private let variables = [
        "name": "Denidu Thiranjaya Gamage",
        "age": 23
    ] as [String: Any]
    
    private let platforms = [
        "LinkedIn": "www.linkedin.com/in/denidu",
        "Email": "denidugamage21@gmail.com"
    ]

    var body: some View {
        VStack(alignment: .leading, spacing: 20) {
            Text(getDescription())
                .font(.headline)
                .padding()

            Divider()

            Text(getSocialMedias())
                .font(.subheadline)
                .padding()

            Spacer()
        }
        .padding()
        .navigationTitle("Denidu Info")
    }

    private func getDescription() -> String {
        var description = "---deniduu---\n"
        for (index, value) in variables.values.enumerated() {
            switch index {
            case 0:
                description += "Name: \(value)\n"
            case 1:
                description += "Age: \(value)\n"
            default:
                break
            }
        }
        return description
    }

    private func getSocialMedias() -> String {
        var contact = "\n-----contact-----\n"
        for (key, value) in platforms {
            contact += "\(key): \(value)\n"
        }
        return contact
    }
}

struct ContentView: View {
    var body: some View {
        NavigationView {
            DeniduView()
        }
    }
}

@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            ContentView()
        }
    }
}


</pre>
