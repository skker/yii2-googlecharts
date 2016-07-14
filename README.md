Google Charts Extension for Yii 2
===============================

[![Latest Stable Version](https://poser.pugx.org/bsadnu/yii2-googlecharts/v/stable)](https://packagist.org/packages/bsadnu/yii2-googlecharts) [![Total Downloads](https://poser.pugx.org/bsadnu/yii2-googlecharts/downloads)](https://packagist.org/packages/bsadnu/yii2-googlecharts) [![Latest Unstable Version](https://poser.pugx.org/bsadnu/yii2-googlecharts/v/unstable)](https://packagist.org/packages/bsadnu/yii2-googlecharts) [![License](https://poser.pugx.org/bsadnu/yii2-googlecharts/license)](https://packagist.org/packages/bsadnu/yii2-googlecharts)

This extension contains a lot of chart widgets based on [Google Charts API](https://developers.google.com/chart/).

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist bsadnu/yii2-googlecharts "*"
```

or add

```json
"bsadnu/yii2-googlecharts": "*"
```

to the require section of your composer.json.

Usage
-----

To use any of these widgets,  simply add the following code in your view.

### Column Chart Example
```php
...
use bsadnu\googlecharts\ColumnChart;
...
```
1) Simple Column Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/ColumnChartSimple.png)
```php
<?= ColumnChart::widget([
	'id' => 'my-column-chart-id',
    'data' => [
        ['Year', 'Sales', 'Expenses'],
        ['2013',  1000,      400],
        ['2014',  1170,      460],
        ['2015',  660,       1120],
        ['2016',  1030,      540]
    ],
    'options' => [
        'fontName' => 'Verdana',
        'height' => 400,
        'fontSize' => 12,
        'chartArea' => [
        	'left' => '5%',
        	'width' => '90%',
        	'height' => 350
        ],
        'tooltip' => [
        	'textStyle' => [
        		'fontName' => 'Verdana',
        		'fontSize' => 13
        	]
        ],
        'vAxis' => [
        	'title' => 'Sales and Expenses',
        	'titleTextStyle' => [
        		'fontSize' => 13,
        		'italic' => false
        	],
        	'gridlines' => [
        		'color' => '#e5e5e5',
        		'count' => 10
        	],            	
        	'minValue' => 0
        ],
        'legend' => [
        	'position' => 'top',
        	'alignment' => 'center',
        	'textStyle' => [
        		'fontSize' => 12
        	]
        ]            
    ]
]) ?>
```

2) Stacked Column Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/ColumnChartStacked.png)
```php
<?= ColumnChart::widget([
	'id' => 'my-stacked-column-chart-id',
    'data' => [
		['Genre', 'Fantasy & Sci Fi', 'Romance', 'Mystery/Crime', 'General', 'Western', 'Literature'],
		['2000', 20, 30, 35, 40, 45, 30],
		['2005', 14, 20, 25, 30, 48, 30],
		['2010', 10, 24, 20, 32, 18, 5],
		['2015', 15, 25, 30, 35, 20, 15],
		['2020', 16, 22, 23, 30, 16, 9],
		['2025', 12, 26, 20, 40, 20, 30],
		['2030', 28, 19, 29, 30, 12, 13]
    ],
    'options' => [
        'fontName' => 'Verdana',
        'height' => 400,
        'fontSize' => 12,
        'chartArea' => [
        	'left' => '5%',
        	'width' => '90%',
        	'height' => 350
        ],
        'isStacked' => true,
        'tooltip' => [
        	'textStyle' => [
        		'fontName' => 'Verdana',
        		'fontSize' => 13
        	]
        ],
        'vAxis' => [
        	'title' => 'Sales and Expenses',
        	'titleTextStyle' => [
        		'fontSize' => 13,
        		'italic' => false
        	],
        	'gridlines' => [
        		'color' => '#e5e5e5',
        		'count' => 10
        	],            	
        	'minValue' => 0
        ],
        'legend' => [
        	'position' => 'top',
        	'alignment' => 'center',
        	'textStyle' => [
        		'fontSize' => 12
        	]
        ]            
    ]
]) ?>
```

### Bar Chart Example
```php
...
use bsadnu\googlecharts\BarChart;
...
```
1) Simple Bar Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/BarChart.png)
```php
<?= BarChart::widget([
	'id' => 'my-bar-chart-id',
    'data' => [
        ['Year', 'Sales', 'Expenses'],
        ['2004',  1000,      400],
        ['2005',  1170,      460],
        ['2006',  660,       1120],
        ['2007',  1030,      540]
    ],
    'options' => [
        'fontName' => 'Verdana',
        'height' => 400,
        'fontSize' => 12,
        'chartArea' => [
        	'left' => '5%',
        	'width' => '90%',
        	'height' => 350
        ],
        'tooltip' => [
        	'textStyle' => [
        		'fontName' => 'Verdana',
        		'fontSize' => 13
        	]
        ],
        'vAxis' => [
        	'gridlines' => [
        		'color' => '#e5e5e5',
        		'count' => 10
        	],            	
        	'minValue' => 0
        ],
        'legend' => [
        	'position' => 'top',
        	'alignment' => 'center',
        	'textStyle' => [
        		'fontSize' => 12
        	]
        ]            
    ]
]) ?>
```

2) Stacked Bar Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/BarChartStacked.png)
```php
<?= BarChart::widget([
	'id' => 'my-stacked-bar-chart-id',
    'data' => [
		['Genre', 'Fantasy & Sci Fi', 'Romance', 'Mystery/Crime', 'General', 'Western', 'Literature'],
		['2000', 20, 30, 35, 40, 45, 30],
		['2005', 14, 20, 25, 30, 48, 30],
		['2010', 10, 24, 20, 32, 18, 5],
		['2015', 15, 25, 30, 35, 20, 15],
		['2020', 16, 22, 23, 30, 16, 9],
		['2025', 12, 26, 20, 40, 20, 30],
		['2030', 28, 19, 29, 30, 12, 13]
    ],
    'options' => [
        'fontName' => 'Verdana',
        'height' => 400,
        'fontSize' => 12,
        'chartArea' => [
        	'left' => '5%',
        	'width' => '90%',
        	'height' => 350
        ],
        'isStacked' => true,
        'tooltip' => [
        	'textStyle' => [
        		'fontName' => 'Verdana',
        		'fontSize' => 13
        	]
        ],
        'hAxis' => [
        	'gridlines' => [
        		'color' => '#e5e5e5',
        		'count' => 10
        	],            	
        	'minValue' => 0
        ],
        'legend' => [
        	'position' => 'top',
        	'alignment' => 'center',
        	'textStyle' => [
        		'fontSize' => 12
        	]
        ]            
    ]
]) ?>
```

### Histogram Example
```php
...
use bsadnu\googlecharts\Histogram;
...
```
![demo](https://dl.dropboxusercontent.com/u/94373707/Histogram.png)
```php
<?= Histogram::widget([
	'id' => 'my-simple-histogram-id',
	'data' => [
		['Dinosaur', 'Length'],
		['Acrocanthosaurus (top-spined lizard)', 12.2],
		['Albertosaurus (Alberta lizard)', 9.1],
		['Allosaurus (other lizard)', 12.2],
		['Apatosaurus (deceptive lizard)', 22.9],
		['Archaeopteryx (ancient wing)', 0.9],
		['Argentinosaurus (Argentina lizard)', 36.6],
		['Baryonyx (heavy claws)', 9.1],
		['Brachiosaurus (arm lizard)', 30.5],
		['Ceratosaurus (horned lizard)', 6.1],
		['Coelophysis (hollow form)', 2.7],
		['Compsognathus (elegant jaw)', 0.9],
		['Deinonychus (terrible claw)', 2.7],
		['Diplodocus (double beam)', 27.1],
		['Dromicelomimus (emu mimic)', 3.4],
		['Gallimimus (fowl mimic)', 5.5],
		['Mamenchisaurus (Mamenchi lizard)', 21.0],
		['Megalosaurus (big lizard)', 7.9],
		['Microvenator (small hunter)', 1.2],
		['Ornithomimus (bird mimic)', 4.6],
		['Oviraptor (egg robber)', 1.5],
		['Plateosaurus (flat lizard)', 7.9],
		['Sauronithoides (narrow-clawed lizard)', 2.0],
		['Seismosaurus (tremor lizard)', 45.7],
		['Spinosaurus (spiny lizard)', 12.2],
		['Supersaurus (super lizard)', 30.5],
		['Tyrannosaurus (tyrant lizard)', 15.2],
		['Ultrasaurus (ultra lizard)', 30.5],
		['Velociraptor (swift robber)', 1.8]
	],
	'options' => [
	    'fontName' => 'Verdana',
	    'height' => 400,
	    'fontSize' => 12,
	    'chartArea' => [
	    	'left' => '5%',
	    	'width' => '90%',
	    	'height' => 350
	    ],
	    'isStacked' => true,
	    'tooltip' => [
	    	'textStyle' => [
	    		'fontName' => 'Verdana',
	    		'fontSize' => 13
	    	]
	    ],
	    'vAxis' => [
	    	'title' => 'Dinosaur length',
	    	'titleTextStyle' => [
	    		'fontSize' => 13,
	    		'italic' => false
	    	],        	
	    	'gridlines' => [
	    		'color' => '#e5e5e5',
	    		'count' => 10
	    	],            	
	    	'minValue' => 0
	    ],        
	    'hAxis' => [
	    	'gridlines' => [
	    		'color' => '#e5e5e5'
	    	],            	
	    	'minValue' => 0
	    ],
	    'legend' => [
	    	'position' => 'top',
	    	'alignment' => 'center',
	    	'textStyle' => [
	    		'fontSize' => 12
	    	]
	    ]            
	]
]) ?>
```

### Combo Chart Example
```php
...
use bsadnu\googlecharts\ComboChart;
...
```
![demo](https://dl.dropboxusercontent.com/u/94373707/ComboChart.png)
```php
<?= ComboChart::widget([
	'id' => 'my-combo-chart-id',
	'data' => [
		['Month', 'Bolivia', 'Ecuador', 'Madagascar', 'Papua New Guinea', 'Rwanda', 'Average'],
		['2004/05',  165,      938,         522,             998,           450,      614.6],
		['2005/06',  135,      1120,        599,             1268,          288,      682],
		['2006/07',  157,      1167,        587,             807,           397,      623],
		['2007/08',  139,      1110,        615,             968,           215,      609.4],
		['2008/09',  136,      691,         629,             1026,          366,      569.6]
	],
	'options' => [
	    'fontName' => 'Verdana',
	    'height' => 400,
	    'fontSize' => 12,
	    'chartArea' => [
	    	'left' => '5%',
	    	'width' => '90%',
	    	'height' => 350
	    ],
	    'seriesType' => 'bars',
		'series' => [
			5 => [
				'type' => 'line',
				'pointSize' => 5
			]
		],        
	    'tooltip' => [
	    	'textStyle' => [
	    		'fontName' => 'Verdana',
	    		'fontSize' => 13
	    	]
	    ],
	    'vAxis' => [
	    	'gridlines' => [
	    		'color' => '#e5e5e5',
	    		'count' => 10
	    	],            	
	    	'minValue' => 0
	    ],        
	    'legend' => [
	    	'position' => 'top',
	    	'alignment' => 'center',
	    	'textStyle' => [
	    		'fontSize' => 12
	    	]
	    ]            
	]
]) ?>
```

### Line Chart Example
```php
...
use bsadnu\googlecharts\LineChart;
...
```
1) Simple Line Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/LineChartSimple.png)
```php
<?= LineChart::widget([
	'id' => 'my-simple-line-chart-id',
	'data' => [
		['Year', 'Sales', 'Expenses'],
		['2004',  1000,      400],
		['2005',  1170,      460],
		['2006',  660,       1120],
		['2007',  1030,      540]
	],
	'options' => [
	    'fontName' => 'Verdana',
	    'height' => 400,
	    'curveType' => 'function',
	    'fontSize' => 12,
	    'chartArea' => [
	    	'left' => '5%',
	    	'width' => '90%',
	    	'height' => 350
	    ],
	    'pointSize' => 4,
	    'tooltip' => [
	    	'textStyle' => [
	    		'fontName' => 'Verdana',
	    		'fontSize' => 13
	    	]
	    ],
	    'vAxis' => [
	    	'title' => 'Sales and Expenses',
			'titleTextStyle' => [
				'fontSize' => 13,
				'italic' => false
			],        	
	    	'gridlines' => [
	    		'color' => '#e5e5e5',
	    		'count' => 10
	    	],            	
	    	'minValue' => 0
	    ],        
	    'legend' => [
	    	'position' => 'top',
	    	'alignment' => 'center',
	    	'textStyle' => [
	    		'fontSize' => 12
	    	]
	    ]            
	]
]) ?>
```

2) Line Intervals Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/LineChartIntervals.png)
```php
<?= LineChart::widget([
	'id' => 'my-line-intervals-id',
	'isIntervalType' => true,
	'data' => [
		['a', 100, 90, 110, 85, 96, 104, 120],
		['b', 120, 95, 130, 90, 113, 124, 140],
		['c', 130, 105, 140, 100, 117, 133, 139],
		['d', 90, 85, 95, 85, 88, 92, 95],
		['e', 70, 74, 63, 67, 69, 70, 72],
		['f', 30, 39, 22, 21, 28, 34, 40],
		['g', 80, 77, 83, 70, 77, 85, 90],
		['h', 100, 90, 110, 85, 95, 102, 110]
	],
	'options' => [
		'fontName' => 'Verdana',
		'height' => 400,
		'curveType' => 'function',
		'fontSize' => 12,
		'chartArea' => [
			'left' => '5%',
			'width' => '90%',
			'height' => 350
		],
		'lineWidth' => 3,
		'tooltip' => [
			'textStyle' => [
				'fontName' => 'Verdana',
				'fontSize' => 13
			]
		],
		'series' => [
			[
				'color' => '#EF5350'
			]
		],
		'intervals' => [
			'style' => 'line'
		],
		'pointSize' => 5,	
		'vAxis' => [
			'title' => 'Number values',
			'titleTextStyle' => [
				'fontSize' => 13,
				'italic' => false
			],        	
			'gridlines' => [
				'color' => '#e5e5e5',
				'count' => 10
			],            	
			'minValue' => 0
		],        
		'legend' => 'none'            
	]
]) ?>
```

3) Line Intervals Area Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/LineChartIntervalsArea.png)
```php
<?= LineChart::widget([
	'id' => 'my-area-intervals-id',
	'isIntervalType' => true,
	'data' => [
		['a', 100, 90, 110, 85, 96, 104, 120],
		['b', 120, 95, 130, 90, 113, 124, 140],
		['c', 130, 105, 140, 100, 117, 133, 139],
		['d', 90, 85, 95, 85, 88, 92, 95],
		['e', 70, 74, 63, 67, 69, 70, 72],
		['f', 30, 39, 22, 21, 28, 34, 40],
		['g', 80, 77, 83, 70, 77, 85, 90],
		['h', 100, 90, 110, 85, 95, 102, 110]
	],
	'options' => [
		'fontName' => 'Verdana',
		'height' => 400,
		'curveType' => 'function',
		'fontSize' => 12,
		'chartArea' => [
			'left' => '5%',
			'width' => '90%',
			'height' => 350
		],
		'lineWidth' => 2,
		'tooltip' => [
			'textStyle' => [
				'fontName' => 'Verdana',
				'fontSize' => 13
			]
		],
		'series' => [
			[
				'color' => '#43A047'
			]
		],
		'intervals' => [
			'style' => 'area'
		],
		'pointSize' => 5,	
		'vAxis' => [
			'title' => 'Number values',
			'titleTextStyle' => [
				'fontSize' => 13,
				'italic' => false
			],        	
			'gridlines' => [
				'color' => '#e5e5e5',
				'count' => 10
			],            	
			'minValue' => 0
		],        
		'legend' => 'none'            
	]
]) ?>
```

### Area Chart Example
```php
...
use bsadnu\googlecharts\AreaChart;
...
```
1) Simple Area Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/AreaChart.png)
```php
<?= AreaChart::widget([
	'id' => 'my-simple-area-chart-id',
    'data' => [
		['Year', 'Sales', 'Expenses'],
		['2004',  1000,      400],
		['2005',  1170,      460],
		['2006',  660,       1120],
		['2007',  1030,      540]
    ],
    'options' => [
        'fontName' => 'Verdana',
        'height' => 400,
        'curveType' => 'function',
        'fontSize' => 12,
        'areaOpacity' => 0.4,
        'chartArea' => [
        	'left' => '5%',
        	'width' => '90%',
        	'height' => 350
        ],
        'pointSize' => 4,
        'tooltip' => [
        	'textStyle' => [
        		'fontName' => 'Verdana',
        		'fontSize' => 13
        	]
        ],
        'vAxis' => [
        	'title' => 'Sales and Expenses',
			'titleTextStyle' => [
				'fontSize' => 13,
				'italic' => false
			],        	
        	'gridarea' => [
        		'color' => '#e5e5e5',
        		'count' => 10
        	],            	
        	'minValue' => 0
        ],        
        'legend' => [
        	'position' => 'top',
        	'alignment' => 'end',
        	'textStyle' => [
        		'fontSize' => 12
        	]
        ]            
    ]
]) ?>
```

2) Stacked Area Chart

![demo](https://dl.dropboxusercontent.com/u/94373707/AreaChartStacked.png)
```php
<?= AreaChart::widget([
	'id' => 'my-staked-area-chart-id',
	'data' => [
		['Year', 'Cars', 'Trucks', 'Drones', 'Segways'],
		['2013',  870,  460, 310, 220],
		['2014',  460,  720, 220, 460],
		['2015',  930,  640, 340, 330],
		['2016',  1000,  400, 180, 500]
	],
	'options' => [
		'fontName' => 'Verdana',
		'height' => 400,
		'curveType' => 'function',
		'fontSize' => 12,
		'areaOpacity' => 0.4,
		'chartArea' => [
			'left' => '5%',
			'width' => '90%',
			'height' => 350
		],
		'isStacked' => true,
		'pointSize' => 4,
		'tooltip' => [
			'textStyle' => [
				'fontName' => 'Verdana',
				'fontSize' => 13
			]
		],
		'lineWidth' => 1.5,
		'vAxis' => [
			'title' => 'Number values',
			'titleTextStyle' => [
				'fontSize' => 13,
				'italic' => false
			],        	
			'gridlines' => [
				'color' => '#e5e5e5',
				'count' => 10
			],            	
			'minValue' => 0
		],        
		'legend' => [
			'position' => 'top',
			'alignment' => 'end',
			'textStyle' => [
				'fontSize' => 12
			]
		]            
	]
]) ?>
```

### Stepped Area Chart Example
```php
...
use bsadnu\googlecharts\SteppedAreaChart;
...
```
![demo](https://dl.dropboxusercontent.com/u/94373707/SteppedAreaChart.png)
```php
<?= SteppedAreaChart::widget([
	'id' => 'my-stepped-area-chart-id',
	'data' => [
		['Director (Year)',  'Rotten Tomatoes', 'IMDB'],
		['Alfred Hitchcock (1935)', 8.4,         7.9],
		['Ralph Thomas (1959)',     6.9,         6.5],
		['Don Sharp (1978)',        6.5,         6.4],
		['James Hawes (2008)',      4.4,         6.2]
	],
	'options' => [
		'fontName' => 'Verdana',
		'height' => 400,
		'isStacked' => true,
		'fontSize' => 12,
		'chartArea' => [
			'left' => '5%',
			'width' => '90%',
			'height' => 350
		],
		'lineWidth' => 1,
		'tooltip' => [
			'textStyle' => [
				'fontName' => 'Verdana',
				'fontSize' => 13
			]
		],
		'pointSize' => 5,	
		'vAxis' => [
			'title' => 'Accumulated Rating',
			'titleTextStyle' => [
				'fontSize' => 13,
				'italic' => false
			],        	
			'gridlines' => [
				'color' => '#e5e5e5',
				'count' => 10
			],            	
			'minValue' => 0
		],        
		'legend' => [
			'position' => 'top',
			'alignment' => 'center',
			'textStyle' => [
				'fontSize' => 12
			]
		]            
	]
]) ?>
```

### Pie Chart Example
```php
...
use bsadnu\googlecharts\PieChart;
...
```
![demo](https://dl.dropboxusercontent.com/u/94373707/PieChart.png)
```php
<?= PieChart::widget([
    'id' => 'my-pie-chart-id',
    'data' => [
        ['Major', 'Degrees'],
        ['Business', 256070],
        ['Education', 108034],
        ['Social Sciences & History', 127101],
        ['Health', 81863],
        ['Psychology', 74194]
    ],
    'extraData' => [
        ['Major', 'Degrees'],
        ['Business', 358293],
        ['Education', 101265],
        ['Social Sciences & History', 172780],
        ['Health', 129634],
        ['Psychology', 97216]
    ],                
    'options' => [
        'fontName' => 'Verdana',
        'height' => 300,
        'width' => 500,
        'chartArea' => [
            'left' => 50,
            'width' => '90%',
            'height' => '90%'
        ],
        'diff' => [
            'extraData' => [
                'inCenter' => false
            ]
        ]
    ]
]) ?>
```

## License

**yii2-googlecharts** is released under the BSD 2-Clause License. See the bundled [LICENSE](https://github.com/bsadnu/yii2-googlecharts/blob/master/LICENSE) for details.
