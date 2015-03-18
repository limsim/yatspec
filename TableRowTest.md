# Example #

```
@RunWith(TableRunner.class)
public class TableExampleTest {
    @Test
    @Table({@Row({"The quick brown fox jumps over the lazy dog", "fox"}),
            @Row({"Sator Arepo Tenet Opera Rotas", "Opera"})})
    public void demonstratingPassingMuiltipleArguments(String phrase, String word){
        assertThat(phrase, contains(word));
    }
}
```

# Details #

The test will be run 2 times passing in the phrase and word associated with each row

# Limitations #

Due to Java annotations being a pretty poor copy of .NET Attributes, you can't have multiple instances of the same annotation (hence the table wrapper annotation). Also, Java annotations don't support any types of than the java lang primitives + String.

# Future #

The plan is to support strong typing by also supporting a non-annotation based table setup.