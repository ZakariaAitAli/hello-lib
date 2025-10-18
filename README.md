# ☕ hello-lib

A minimal **Java / Maven library** published to **GitHub Packages**.

## 📦 Usage

Add this to your `pom.xml`:

```xml
<repositories>
  <repository>
    <id>github</id>
    <url>https://maven.pkg.github.com/ZakariaAitAli/hello-lib</url>
  </repository>
</repositories>

<dependencies>
  <dependency>
    <groupId>com.zakaria</groupId>
    <artifactId>hello-lib</artifactId>
    <version>1.0.0</version>
  </dependency>
</dependencies>
````

Then in Java:

```java
import com.zakaria.Hello;

public class Test {
    public static void main(String[] args) {
        System.out.println(Hello.sayHello("Zakaria"));
    }
}
```

---

## 🚀 Publishing

Authenticate Maven with your **GitHub personal access token**:

```bash
export GITHUB_TOKEN=your_token
```

Then create or edit `~/.m2/settings.xml`:

```xml
<settings>
  <servers>
    <server>
      <id>github</id>
      <username>zakariaaitali</username>
      <password>${env.GITHUB_TOKEN}</password>
    </server>
  </servers>
</settings>
```

Finally, publish your package:

```bash
mvn deploy
```
