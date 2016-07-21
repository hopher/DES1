**使用方法**

```
$key = 'your encode key';

$des = new DES1($key);
$result = $des->decrypt($q);
// 把 a=1&b=2 转成数组
parse_str($result, $_data);

function parse_url_decode($key, $q_str = '')
{
    if ($q_str == '')
        return '';
    $des = new DES1($key);
    $result = $des->decrypt($q_str);
    return $result;
}

function parse_url_encode($key, $q_str = '')
{
    if ($q_str == '')
        return '';
    $des = new DES1($key);
    $result = $des->encrypt($q_str);
    return $result;
}
```