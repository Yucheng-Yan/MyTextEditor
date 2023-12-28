# MyTextEditor
## Step 4
```#include <unistd.h>

int main() {
  char c;
  /* Because the return value of read is how many bytes did it read, and "1" after "&c" specifies that the read() function only reads one byte once a time. Hence, this read() function will always return 1*/

  /* The second parameter of read() is a pointer pointing to an address that will store the content read from STDIN_FILENO*/
  while (read(STDIN_FILENO, &c, 1) == 1 && c != 'q');
  return 0;
}```