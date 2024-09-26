# Inertia 定义字段

```php
[
  title 						=>	页面标题
  list_info   			=>	XXX::collection($list)    // 行数据
  single_actions		=>  [													// 行操作
    [
      'label'  => 单行操作名字
      'action' => 单行操作行为对应调用的后端方法
      'method' => 调用后端接口的方法
      'request_name' => 调用后端接口方法定义的name
      'router_params' => 调用路径参数
      'body_params' =>  [       // 调用请求体需要传递的参数
        xxx_key1 => [
          type  => number | text | single_choice | file
          label => 字段名字
          key  => xxx_key1
        ]
      ]
    ]
  ]
  multi_actions		=> []    //  多行操作
  table_actions   => [
    [
      'label' => '导入',
      'action' => 'import',
      'method' => 'post',
      'request_name' => 'period.import',
      'request_form' => 'formData',
      'router_params' => '',
      'body_params' => [
          'file' => [
              'type' => 'file',
              'label' => '文件',
              'data_type' => 'base64Data',
          ],
          'name' => [
              'type' => 'text',
              'label' => '文件名',
          ],
          'import_type' => [
              'type' => 'single_choice',
              'label' => '导入类型',
              'options' => [
                  ['label' => '商品成本', 'value' => 'product_cost'],
                  ['label' => '履约成本', 'value' => 'fulfillment_cost'],
                  ['label' => '支付账单', 'value' => 'payment_cost'],
              ],
          ],
      ]
    ],
    [
			'label' => '结账导出',
      'action' => 'endExport',
      'method' => 'get',
      'request_name' => 'period.end.export',
      'router_params' => '',
    ]
  ],
  'list_header' => [     // 列头部信息
      "事业部",
      "业务类型",
      "会计期间",
      "结账状态",
      "执行状态",
      "执行信息"
  ],
  'list_key' => [         // 列信息对应了数据集中的那个字段
      "business_divisions_code",
      "business_type_code",
      "period_ym",
      "status_des",
      "exe_status_des",
      "exe_msg"
  ],
  'filtersList' => [     // 筛选字段传参
    [
        'type' => 'text',
        'label' => 'Name',
        'key' => 'name',
    ],
    [
        'type' => 'single_choice',
        'label' => '事业部',
        'key' => 'business_divisions_code',
        'options' => [
            [
                'label' => 'all',
                'value' => ' ',
            ],
            [
                'label' => 'Global',
                'value' => 'global',
            ],
            [
                'label' => 'South Korea',
                'value' => 'korea',
            ],
            [
                'label' => 'Japan',
                'value' => 'japan',
            ],
            [
                'label' => 'Mexico',
                'value' => 'mexico',
            ],
        ],
    ],
    [
        'type' => 'single_choice_search',
        'label' => '业务类型',
        'key' => 'business_type_code',
        'options' => [
            [
                'value' => 'dtc',
                'label' => 'DTC',
            ],
            [
                'value' => 'mpl',
                'label' => 'MPL',
            ],
            [
                'value' => 'b2b',
                'label' => 'B2B',
            ],
            [
                'value' => 'b2c',
                'label' => 'B2C',
            ],
            [
                'value' => 'marketing',
                'label' => 'MKT',
            ],
        ],
    ],
    [
        'type' => 'multi_choice',
        'label' => '账期',
        'key' => 'period_ym',
        'options' => [
            ['label' => '2023-07', 'value' => '2023-07'],
            ['label' => '2023-08', 'value' => '2023-08'],
            ['label' => '2023-09', 'value' => '2023-09'],
            ['label' => '2023-10', 'value' => '2023-10'],
            ['label' => '2023-11', 'value' => '2023-11'],
            ['label' => '2023-12', 'value' => '2023-12'],
            ['label' => '2024-01', 'value' => '2024-01'],
            ['label' => '2024-02', 'value' => '2024-02'],
            ['label' => '2024-03', 'value' => '2024-03'],
            ['label' => '2024-04', 'value' => '2024-04'],
            ['label' => '2024-05', 'value' => '2024-05'],
            ['label' => '2024-06', 'value' => '2024-06'],
            ['label' => '2024-07', 'value' => '2024-07'],
        ],
    ],
    [
        'type' => 'date_range',
        'label' => '时间筛选',
        'key' => 'date_range',
    ],
]
]


```

