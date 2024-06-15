# Kafka-Mini-Project

This is a docker project that creates a kafka single node cluster in a docker container with a zookeeper. And also creates a 2 container docker application with a kafka producer and consumer that interact with one another.

## Project Structure
```
.
├── docker-compose.yml
├── docker-compose.kafka.yml
├── README.md
├── detector
│ ├── Dockerfile
│ ├── app.py
│ └── requirements.txt
└── generator
│ ├── Dockerfile
│ ├── app.py
│ └── requirements.txt
```

### Sample Output
``` terminal
detector-1   | streaming.transactions.legit {'source': 'TAEgSHfg2IFI', 'target': 'Dq3fQUEh8KiZ', 'amount': 372.56, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'fSZ2C8KiCGIP', 'target': 'nrIAmDfvPtwI', 'amount': 3735.71, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'lTP85vZQGcev', 'target': '3Dw3U63PCAry', 'amount': 7589.58, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': '1CvuV9mjgDjc', 'target': 'MAfhfQkZmZZ3', 'amount': 9394.92, 'currency': 'USD'}
generator-1  | {'source': 'vnAIy4u2GW2V', 'target': 'L0z40u358P2n', 'amount': 2479.73, 'currency': 'USD'}
generator-1  | {'source': 'kwAdiZRMoIcv', 'target': 'gAF0vkRBxNJk', 'amount': 7805.3, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'os7Znfspq23I', 'target': 'Mv5NWqJmOxmu', 'amount': 8671.74, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': '7pyE02If7dcq', 'target': 'HJdrmkTFQRgS', 'amount': 6540.09, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'WYt51NCXpRKh', 'target': 'rb9eAfK7cFOc', 'amount': 1400.01, 'currency': 'USD'}
detector-1   | streaming.transactions.legit {'source': 'plNMcUADb3rF', 'target': 'sFdjXlKsgWMp', 'amount': 224.16, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'TxtkRgaMBrk8', 'target': '4eXXmiJfkOAt', 'amount': 2897.13, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'zVFfxBoz7v3a', 'target': 'scN6Hp8cl1DG', 'amount': 3819.36, 'currency': 'USD'}
generator-1  | {'source': '3rFarl4sHVy5', 'target': 'xKz57nDC7ENi', 'amount': 7539.82, 'currency': 'USD'}
generator-1  | {'source': 'f8HIC79uxvgz', 'target': 'LZHXC9I41Bo9', 'amount': 541.03, 'currency': 'USD'}
generator-1  | {'source': 'DL9UXyq8UrHv', 'target': 'mgaTQBNodoHZ', 'amount': 2266.45, 'currency': 'USD'}
generator-1  | {'source': 'ZpAO75wOMZi3', 'target': 'OI7M8UZYbovH', 'amount': 5930.81, 'currency': 'USD'}
generator-1  | {'source': 'ptm7MGLIQSTg', 'target': 'Z2y9eHBaG18v', 'amount': 9925.48, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'Qmlhyr5UXFkd', 'target': 'y4ilQXstdljr', 'amount': 2655.81, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'uNtRAJyP30k3', 'target': '4FfC5rCSRziu', 'amount': 5914.61, 'currency': 'USD'}
generator-1  | {'source': 'FCx2jQ59qNYt', 'target': 'xw73BVancDkM', 'amount': 2960.87, 'currency': 'USD'}
generator-1  | {'source': '7P8JcFUzEdF5', 'target': 'ty1BIcbskhaH', 'amount': 5716.69, 'currency': 'USD'}
generator-1  | {'source': 'knRxFQJqolLx', 'target': 'mnby1lSjdnHc', 'amount': 7488.87, 'currency': 'USD'}
generator-1  | {'source': 'PrRoZAGCwQz1', 'target': 'uNiqUzp9YwsV', 'amount': 489.4, 'currency': 'USD'}
generator-1  | {'source': 'sG1mdoBVSoyN', 'target': 'ydfcQ8d2oZjw', 'amount': 7136.5, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'sYH62RgjSbHd', 'target': 'b0iJdRGhxFsx', 'amount': 5197.96, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'K8XxL5gYxTr3', 'target': 'S1RJus6zk3Uc', 'amount': 9497.1, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'Hx6fwau2LEWp', 'target': 'yHD4L7M9P7rA', 'amount': 4408.92, 'currency': 'USD'}
detector-1   | streaming.transactions.legit {'source': 'TY2Biq3eQrel', 'target': 'LPXeErGyQKho', 'amount': 414.12, 'currency': 'USD'}
generator-1  | {'source': 'jS7dlAeGsfHK', 'target': 'spoJw85JM2wL', 'amount': 4201.67, 'currency': 'USD'}
generator-1  | {'source': 'ZlKMx9YOB92k', 'target': 'dOVbm5I0W4g2', 'amount': 735.98, 'currency': 'USD'}
generator-1  | {'source': '24CddmKQYAxV', 'target': 'Tp0IHkGhu0Mb', 'amount': 330.78, 'currency': 'USD'}
generator-1  | {'source': '4qn1l8nBHc73', 'target': 'KGWZDcUaYrME', 'amount': 202.94, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'BJbei2AcmzOL', 'target': 'GhkHRNdaTulE', 'amount': 8213.49, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'OM3nLTks7L9p', 'target': 'Aot6uBaS43h6', 'amount': 1924.63, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'rbvfc8JY9b3V', 'target': 'LpcvHymBVKaF', 'amount': 2486.03, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': '9DxlIi2UKCP5', 'target': 'Vaw8PbUdaV92', 'amount': 5824.25, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'gGTZDmdA8wJc', 'target': 'FP0bvOmuE0Y3', 'amount': 8958.3, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'P5yyIwLH3XNB', 'target': 'JcgcsiVWe2d8', 'amount': 5211.84, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': '403cB8wFAE3M', 'target': 'TVkcsiEpTNGw', 'amount': 4730.79, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'uw2FuVnjhP6v', 'target': 'oMvet4DDzKbB', 'amount': 4051.78, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'ZIRgblmJZyNy', 'target': 'McwXZk9q9vKg', 'amount': 1703.97, 'currency': 'USD'}
generator-1  | {'source': 'XHgNiLzOCLis', 'target': 'mgoo45zTzVpM', 'amount': 3275.37, 'currency': 'USD'}
generator-1  | {'source': 'KTean319pEVS', 'target': 'gSdqKwQU3aIk', 'amount': 498.28, 'currency': 'USD'}
generator-1  | {'source': 'MYtadniEQf1a', 'target': 'ZMX4lr4NczmR', 'amount': 9433.1, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'XnFWgW5KIMfE', 'target': 'V92fQFwISYVQ', 'amount': 7780.01, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'U0mYldUnAFHm', 'target': 'BrryuYXt4CRs', 'amount': 2599.94, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': '9eMebXvvoXrH', 'target': '9dalOzG8pR0S', 'amount': 7320.63, 'currency': 'USD'}
generator-1  | {'source': 'TAEgSHfg2IFI', 'target': 'Dq3fQUEh8KiZ', 'amount': 372.56, 'currency': 'USD'}
generator-1  | {'source': 'fSZ2C8KiCGIP', 'target': 'nrIAmDfvPtwI', 'amount': 3735.71, 'currency': 'USD'}
generator-1  | {'source': 'lTP85vZQGcev', 'target': '3Dw3U63PCAry', 'amount': 7589.58, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'qDVvWvBG7uQC', 'target': 'DkQpj7dEyZ1A', 'amount': 1201.7, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'tDtTK92qPY54', 'target': 'US9TE6m4xLIR', 'amount': 9620.56, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'XFIMM3TBiJwh', 'target': 'j2FY82xYSksC', 'amount': 1761.91, 'currency': 'USD'}
detector-1   | streaming.transactions.fraud {'source': 'gPLecjyHkzwk', 'target': 'Rjkd0IOv0Hk2', 'amount': 8522.71, 'currency': 'USD'}
detector-1   | streaming.transactions.legit {'source': 'Sw2JQ31gc4sG', 'target': 'gGpPCHWRIguT', 'amount': 584.34, 'currency': 'USD'}
```