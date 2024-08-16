### Hi there 👋

<pre>

import android.os.Bundle
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class DeniduActivity : AppCompatActivity() {

    private val variables = mapOf(
        "name" to "Denidu Thiranjaya Gamage",
        "age" to 23
    )

    private val platforms = mapOf(
        "LinkedIn" to "www.linkedin.com/in/denidu",
        "Email" to "denidugamage21@gmail.com"
    )

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_denidu)

        val descriptionTextView = findViewById<TextView>(R.id.descriptionTextView)
        val contactTextView = findViewById<TextView>(R.id.contactTextView)

        descriptionTextView.text = getDescription()
        contactTextView.text = getSocialMedias()
    }

    private fun getDescription(): String {
        val stringBuilder = StringBuilder()
        stringBuilder.append("---deniduu---\n")
        variables.values.forEachIndexed { index, value ->
            when (index) {
                0 -> stringBuilder.append("Name: $value\n")
                1 -> stringBuilder.append("Age: $value\n")
            }
        }
        return stringBuilder.toString()
    }

    private fun getSocialMedias(): String {
        val stringBuilder = StringBuilder()
        stringBuilder.append("\n-----contact-----\n")
        platforms.forEach { (key, value) ->
            stringBuilder.append("$key: $value\n")
        }
        return stringBuilder.toString()
    }
}


</pre>
