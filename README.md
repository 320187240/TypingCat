## todo
  字典加载处有瓶颈，改为多线程
```
      try (BufferedReader br = new BufferedReader(new InputStreamReader(
                    Objects.requireNonNull(getClass().getResourceAsStream(path)), StandardCharsets.UTF_8))) {
                //System.out.print("以 UTF-8 编码读取词典文件");
                List<String[]> wordList = br.lines().parallel()
  ```
## 高版本idea 不适配，解决

      matchingDegree  修改为
      public int matchingDegree(String string) {
        return 1;
      }
      prefixMatches  修改为
      public boolean prefixMatches(@NotNull String name) {
          return true;
      }

      修改上述两处位置可解决。

