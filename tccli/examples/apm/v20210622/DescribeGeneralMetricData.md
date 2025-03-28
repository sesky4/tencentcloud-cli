**Example 1: 查询1分钟聚合粒度的 service_metric 指标数据示例**

该示例查询业务系统为 apm-059oXBfTL，按照 service.name（应用名）、span.kind（客户端/服务端视角）为维度过滤，以 service.name（应用名）、span.kind（客户端/服务端视角）进行聚合，查找开始时间-终止时间内以一分钟为聚合粒度的 request_count（请求数量）、error_request_count（错误请求数量）、duration_avg（平均响应时间）、slow_request_count（慢请求数量）、duration_p50（耗时 p50）的指标数据。

Input: 

```
tccli apm DescribeGeneralMetricData --cli-unfold-argument  \
    --Filters.0.Key service.name \
    --Filters.0.Value ot-java-order-service \
    --Filters.1.Key span.kind \
    --Filters.1.Value client \
    --ViewName service_metric \
    --InstanceId apm-059oXBfTL \
    --Period 60 \
    --Metrics request_count error_request_count duration_avg slow_request_count duration_p50 \
    --StartTime 1734415200 \
    --EndTime 1734418800 \
    --GroupBy service.name span.kind
```

Output: 
```
{
    "Response": {
        "Records": [
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "request_count",
                "MetricNameCN": "总请求数",
                "TimeSerial": [
                    1734415200,
                    1734415260,
                    1734415320,
                    1734415380,
                    1734415440,
                    1734415500,
                    1734415560,
                    1734415620,
                    1734415680,
                    1734415740,
                    1734415800,
                    1734415860,
                    1734415920,
                    1734415980,
                    1734416040,
                    1734416100,
                    1734416160,
                    1734416220,
                    1734416280,
                    1734416340,
                    1734416400,
                    1734416460,
                    1734416520,
                    1734416580,
                    1734416640,
                    1734416700,
                    1734416760,
                    1734416820,
                    1734416880,
                    1734416940,
                    1734417000,
                    1734417060,
                    1734417120,
                    1734417180,
                    1734417240,
                    1734417300,
                    1734417360,
                    1734417420,
                    1734417480,
                    1734417540,
                    1734417600,
                    1734417660,
                    1734417720,
                    1734417780,
                    1734417840,
                    1734417900,
                    1734417960,
                    1734418020,
                    1734418080,
                    1734418140,
                    1734418200,
                    1734418260,
                    1734418320,
                    1734418380,
                    1734418440,
                    1734418500,
                    1734418560,
                    1734418620,
                    1734418680,
                    1734418740
                ],
                "DataSerial": [
                    22,
                    32,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    32,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    26,
                    28,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    32,
                    12,
                    22,
                    22,
                    32,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    22,
                    32,
                    22,
                    12,
                    22,
                    22
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    },
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    }
                ],
                "MetricName": "error_request_count",
                "MetricNameCN": "异常数量",
                "TimeSerial": [
                    1734415200,
                    1734415260,
                    1734415320,
                    1734415380,
                    1734415440,
                    1734415500,
                    1734415560,
                    1734415620,
                    1734415680,
                    1734415740,
                    1734415800,
                    1734415860,
                    1734415920,
                    1734415980,
                    1734416040,
                    1734416100,
                    1734416160,
                    1734416220,
                    1734416280,
                    1734416340,
                    1734416400,
                    1734416460,
                    1734416520,
                    1734416580,
                    1734416640,
                    1734416700,
                    1734416760,
                    1734416820,
                    1734416880,
                    1734416940,
                    1734417000,
                    1734417060,
                    1734417120,
                    1734417180,
                    1734417240,
                    1734417300,
                    1734417360,
                    1734417420,
                    1734417480,
                    1734417540,
                    1734417600,
                    1734417660,
                    1734417720,
                    1734417780,
                    1734417840,
                    1734417900,
                    1734417960,
                    1734418020,
                    1734418080,
                    1734418140,
                    1734418200,
                    1734418260,
                    1734418320,
                    1734418380,
                    1734418440,
                    1734418500,
                    1734418560,
                    1734418620,
                    1734418680,
                    1734418740
                ],
                "DataSerial": [
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [
                    1734415200,
                    1734415260,
                    1734415320,
                    1734415380,
                    1734415440,
                    1734415500,
                    1734415560,
                    1734415620,
                    1734415680,
                    1734415740,
                    1734415800,
                    1734415860,
                    1734415920,
                    1734415980,
                    1734416040,
                    1734416100,
                    1734416160,
                    1734416220,
                    1734416280,
                    1734416340,
                    1734416400,
                    1734416460,
                    1734416520,
                    1734416580,
                    1734416640,
                    1734416700,
                    1734416760,
                    1734416820,
                    1734416880,
                    1734416940,
                    1734417000,
                    1734417060,
                    1734417120,
                    1734417180,
                    1734417240,
                    1734417300,
                    1734417360,
                    1734417420,
                    1734417480,
                    1734417540,
                    1734417600,
                    1734417660,
                    1734417720,
                    1734417780,
                    1734417840,
                    1734417900,
                    1734417960,
                    1734418020,
                    1734418080,
                    1734418140,
                    1734418200,
                    1734418260,
                    1734418320,
                    1734418380,
                    1734418440,
                    1734418500,
                    1734418560,
                    1734418620,
                    1734418680,
                    1734418740
                ],
                "DataSerial": [
                    191.5860133181818,
                    191.2110746363636,
                    191.23246599999996,
                    191.5040949090909,
                    191.934274,
                    192.05015977272723,
                    191.4917418636364,
                    191.7598401818182,
                    191.47329104545454,
                    191.35408840909093,
                    191.7695753181818,
                    192.1501132727273,
                    191.6614135,
                    191.72522395454544,
                    193.92501624242422,
                    209.9224584090909,
                    192.50587436363637,
                    193.14908313636363,
                    200.8337476363636,
                    192.21551695454545,
                    191.87317959090907,
                    191.85476931818184,
                    192.0314575909091,
                    192.14624168181817,
                    192.0624055,
                    192.35865707575758,
                    191.87331737878793,
                    191.806969,
                    192.35163881818187,
                    192.29478813636362,
                    192.3707790454545,
                    191.8557721363636,
                    191.59646177272725,
                    191.55687904545456,
                    191.59595163636365,
                    191.84944554545453,
                    191.78630649999997,
                    191.91973590909092,
                    191.90514081818182,
                    191.9165850909091,
                    191.98103199999997,
                    191.98323287878785,
                    193.0803381818182,
                    192.14093727272729,
                    192.24286899999998,
                    192.6753041818182,
                    192.2717468636364,
                    192.41461836363635,
                    192.3725805,
                    191.84485977272726,
                    191.85852840909092,
                    191.86218731818178,
                    191.6467590454545,
                    191.52699904545452,
                    191.57099809090911,
                    192.2197160909091,
                    191.91881845454546,
                    191.98860699999997,
                    224.0602859090909,
                    192.05223709090907
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "slow_request_count",
                "MetricNameCN": "慢调用",
                "TimeSerial": [
                    1734415200,
                    1734415260,
                    1734415320,
                    1734415380,
                    1734415440,
                    1734415500,
                    1734415560,
                    1734415620,
                    1734415680,
                    1734415740,
                    1734415800,
                    1734415860,
                    1734415920,
                    1734415980,
                    1734416040,
                    1734416100,
                    1734416160,
                    1734416220,
                    1734416280,
                    1734416340,
                    1734416400,
                    1734416460,
                    1734416520,
                    1734416580,
                    1734416640,
                    1734416700,
                    1734416760,
                    1734416820,
                    1734416880,
                    1734416940,
                    1734417000,
                    1734417060,
                    1734417120,
                    1734417180,
                    1734417240,
                    1734417300,
                    1734417360,
                    1734417420,
                    1734417480,
                    1734417540,
                    1734417600,
                    1734417660,
                    1734417720,
                    1734417780,
                    1734417840,
                    1734417900,
                    1734417960,
                    1734418020,
                    1734418080,
                    1734418140,
                    1734418200,
                    1734418260,
                    1734418320,
                    1734418380,
                    1734418440,
                    1734418500,
                    1734418560,
                    1734418620,
                    1734418680,
                    1734418740
                ],
                "DataSerial": [
                    2,
                    3,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    3,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    3,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    3,
                    1,
                    2,
                    2,
                    3,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    2,
                    3,
                    2,
                    1,
                    2,
                    2
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "duration_p50",
                "MetricNameCN": "P50 响应时间",
                "TimeSerial": [
                    1734415200,
                    1734415260,
                    1734415320,
                    1734415380,
                    1734415440,
                    1734415500,
                    1734415560,
                    1734415620,
                    1734415680,
                    1734415740,
                    1734415800,
                    1734415860,
                    1734415920,
                    1734415980,
                    1734416040,
                    1734416100,
                    1734416160,
                    1734416220,
                    1734416280,
                    1734416340,
                    1734416400,
                    1734416460,
                    1734416520,
                    1734416580,
                    1734416640,
                    1734416700,
                    1734416760,
                    1734416820,
                    1734416880,
                    1734416940,
                    1734417000,
                    1734417060,
                    1734417120,
                    1734417180,
                    1734417240,
                    1734417300,
                    1734417360,
                    1734417420,
                    1734417480,
                    1734417540,
                    1734417600,
                    1734417660,
                    1734417720,
                    1734417780,
                    1734417840,
                    1734417900,
                    1734417960,
                    1734418020,
                    1734418080,
                    1734418140,
                    1734418200,
                    1734418260,
                    1734418320,
                    1734418380,
                    1734418440,
                    1734418500,
                    1734418560,
                    1734418620,
                    1734418680,
                    1734418740
                ],
                "DataSerial": [
                    10,
                    10,
                    9.375,
                    14,
                    14,
                    14,
                    10,
                    9.375,
                    9.285714285714285,
                    9.166666666666668,
                    10,
                    14,
                    14,
                    14,
                    15.714285714285714,
                    14.444444444444445,
                    14,
                    14,
                    14.444444444444445,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    13.333333333333332,
                    16.153846153846153,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    15.333333333333332,
                    16.666666666666664,
                    14,
                    14,
                    15.333333333333332,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    14,
                    15.333333333333332,
                    14,
                    10,
                    14.444444444444445,
                    14
                ]
            }
        ],
        "RequestId": "test-test-test"
    }
}
```

**Example 2: 查询起始到终止时间内统计 service_metric 指标数据示例**

该示例查询业务系统为 apm-059oXBfTL，按照 service.name（应用名）、span.kind（客户端/服务端视角）为维度过滤，以 service.name（应用名）、span.kind（客户端/服务端视角）进行聚合，查找开始时间-终止时间内以一分钟为聚合粒度的 request_count（请求数量）、error_request_count（错误请求数量）、duration_avg（平均响应时间）、slow_request_count（慢请求数量）、duration_p50（耗时 p50）的指标数据。

Input: 

```
tccli apm DescribeGeneralMetricData --cli-unfold-argument  \
    --Filters.0.Key service.name \
    --Filters.0.Value ot-java-order-service \
    --Filters.1.Key span.kind \
    --Filters.1.Value client \
    --ViewName service_metric \
    --InstanceId apm-059oXBfTL \
    --Metrics request_count error_request_count duration_avg slow_request_count duration_p50 \
    --StartTime 1734415200 \
    --EndTime 1734418800 \
    --GroupBy service.name span.kind
```

Output: 
```
{
    "Response": {
        "Records": [
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "request_count",
                "MetricNameCN": "总请求数",
                "TimeSerial": [],
                "DataSerial": [
                    1360
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "error_request_count",
                "MetricNameCN": "异常数量",
                "TimeSerial": [],
                "DataSerial": [
                    0
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    192.96957006641412
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "slow_request_count",
                "MetricNameCN": "慢调用",
                "TimeSerial": [],
                "DataSerial": [
                    124
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    },
                    {
                        "Key": "span.kind",
                        "Value": "client"
                    }
                ],
                "MetricName": "duration_p50",
                "MetricNameCN": "P50 响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    13.443708609271523
                ]
            }
        ],
        "RequestId": "test-test-test"
    }
}
```

**Example 3: 查询1分钟聚合粒度的 sql_metric 指标数据示例**

该示例查询业务系统为 apm-059oXBfTL，按照 service.name（应用名）为维度过滤，以 service.name（应用名）进行聚合，查找开始时间-终止时间内以一分钟为聚合粒度的 error_request_count（错误请求数量）、duration_avg（平均响应时间）的指标数据。

Input: 

```
tccli apm DescribeGeneralMetricData --cli-unfold-argument  \
    --Filters.0.Key service.name \
    --Filters.0.Value ot-java-order-service \
    --ViewName sql_metric \
    --InstanceId apm-059oXBfTL \
    --Period 60 \
    --Metrics error_request_count duration_avg \
    --StartTime 1734415200 \
    --EndTime 1734418800 \
    --GroupBy service.name
```

Output: 
```
{
    "Response": {
        "Records": [
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    }
                ],
                "MetricName": "error_request_count",
                "MetricNameCN": "错误数",
                "TimeSerial": [
                    1734415200,
                    1734415260,
                    1734415320,
                    1734415380,
                    1734415440,
                    1734415500,
                    1734415560,
                    1734415620,
                    1734415680,
                    1734415740,
                    1734415800,
                    1734415860,
                    1734415920,
                    1734415980,
                    1734416040,
                    1734416100,
                    1734416160,
                    1734416220,
                    1734416280,
                    1734416340,
                    1734416400,
                    1734416460,
                    1734416520,
                    1734416580,
                    1734416640,
                    1734416700,
                    1734416760,
                    1734416820,
                    1734416880,
                    1734416940,
                    1734417000,
                    1734417060,
                    1734417120,
                    1734417180,
                    1734417240,
                    1734417300,
                    1734417360,
                    1734417420,
                    1734417480,
                    1734417540,
                    1734417600,
                    1734417660,
                    1734417720,
                    1734417780,
                    1734417840,
                    1734417900,
                    1734417960,
                    1734418020,
                    1734418080,
                    1734418140,
                    1734418200,
                    1734418260,
                    1734418320,
                    1734418380,
                    1734418440,
                    1734418500,
                    1734418560,
                    1734418620,
                    1734418680,
                    1734418740
                ],
                "DataSerial": [
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0,
                    0
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [
                    1734415200,
                    1734415260,
                    1734415320,
                    1734415380,
                    1734415440,
                    1734415500,
                    1734415560,
                    1734415620,
                    1734415680,
                    1734415740,
                    1734415800,
                    1734415860,
                    1734415920,
                    1734415980,
                    1734416040,
                    1734416100,
                    1734416160,
                    1734416220,
                    1734416280,
                    1734416340,
                    1734416400,
                    1734416460,
                    1734416520,
                    1734416580,
                    1734416640,
                    1734416700,
                    1734416760,
                    1734416820,
                    1734416880,
                    1734416940,
                    1734417000,
                    1734417060,
                    1734417120,
                    1734417180,
                    1734417240,
                    1734417300,
                    1734417360,
                    1734417420,
                    1734417480,
                    1734417540,
                    1734417600,
                    1734417660,
                    1734417720,
                    1734417780,
                    1734417840,
                    1734417900,
                    1734417960,
                    1734418020,
                    1734418080,
                    1734418140,
                    1734418200,
                    1734418260,
                    1734418320,
                    1734418380,
                    1734418440,
                    1734418500,
                    1734418560,
                    1734418620,
                    1734418680,
                    1734418740
                ],
                "DataSerial": [
                    504.4455225,
                    504.49955074999997,
                    504.50165175000006,
                    504.55699425,
                    504.5483053749999,
                    504.547519,
                    504.73789837500004,
                    504.46199262500005,
                    504.1922,
                    504.22497787500004,
                    504.18011225000004,
                    504.04929475,
                    504.14939112499997,
                    504.45689225,
                    504.4441259166667,
                    504.4853475,
                    504.55031125,
                    504.458504875,
                    504.49732837499994,
                    504.50629599999996,
                    504.439337,
                    504.272122,
                    504.267848625,
                    504.28821525,
                    504.268522875,
                    504.28563437500003,
                    504.25491391666674,
                    504.20538062500003,
                    504.54045425000004,
                    504.67349375000003,
                    504.71599025,
                    504.54132337499993,
                    504.69503825,
                    504.74425037500004,
                    504.637164375,
                    504.62155600000006,
                    504.628113,
                    505.07725949999997,
                    504.65562800000004,
                    504.443061375,
                    504.420146125,
                    504.41736325000005,
                    507.28285875,
                    504.59916025,
                    504.50750687499993,
                    504.67656166666666,
                    504.687698625,
                    504.7468005,
                    504.728723,
                    504.71881125,
                    504.6750935,
                    504.45997087499995,
                    504.48766912499997,
                    504.5063645,
                    504.670277625,
                    504.88526525,
                    505.09475625,
                    505.13066475,
                    505.103745375,
                    505.101275
                ]
            }
        ],
        "RequestId": "test-test-test"
    }
}
```

**Example 4: 查询起始到终止时间内统计 sql_metric 的 duration_avg（耗时时间）指标数据示例**

该示例查询业务系统为apm-059oXBfTL，按照 db.instance（数据库名称）为维度过滤，以 service.name（应用名）、db.statement（执行语句）为维度进行聚合，查找开始时间-终止时间内 top5 的 duration_avg（耗时（ms））的指标数据。

Input: 

```
tccli apm DescribeGeneralMetricData --cli-unfold-argument  \
    --Filters.0.Key db.instance \
    --Filters.0.Value mock_project_db \
    --ViewName sql_metric \
    --InstanceId apm-059oXBfTL \
    --Metrics duration_avg \
    --StartTime 1734415200 \
    --EndTime 1734418800 \
    --GroupBy service.name db.statement \
    --OrderBy.Key sql_duration_avg \
    --OrderBy.Value desc \
    --PageSize 5
```

Output: 
```
{
    "Response": {
        "Records": [
            {
                "Tags": [
                    {
                        "Key": "db.statement",
                        "Value": "select sleep(?)"
                    },
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    2005.583661869444
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "service.name",
                        "Value": "ot-java-stock-service"
                    },
                    {
                        "Key": "db.statement",
                        "Value": "select dept, count(dept) as total from mock_project_userinfo"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    5.746467460185185
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "db.statement",
                        "Value": "select dept, count(dept) as total from mock_project_userinfo"
                    },
                    {
                        "Key": "service.name",
                        "Value": "ot-java-user-service"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    5.719407256481479
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "db.statement",
                        "Value": "select * from mock_project_userinfo"
                    },
                    {
                        "Key": "service.name",
                        "Value": "ot-java-order-service"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    5.677464627777778
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "db.statement",
                        "Value": "select * from mock_project_userinfo"
                    },
                    {
                        "Key": "service.name",
                        "Value": "ot-java-delivery-service"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    5.636013505555556
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "db.statement",
                        "Value": "select * om un_exist_table limit ?"
                    },
                    {
                        "Key": "service.name",
                        "Value": "ot-java-delivery-service"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    5.514262441666669
                ]
            },
            {
                "Tags": [
                    {
                        "Key": "db.statement",
                        "Value": "select dept, count(dept) as total from mock_project_userinfo"
                    },
                    {
                        "Key": "service.name",
                        "Value": "ot-java-market-service"
                    }
                ],
                "MetricName": "duration_avg",
                "MetricNameCN": "平均响应时间",
                "TimeSerial": [],
                "DataSerial": [
                    5.44814345277778
                ]
            }
        ],
        "RequestId": "test-test-test"
    }
}
```

