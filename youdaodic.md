<h2 id="associate">联想</h2>

url：`http://dict.youdao.com/suggest`

拼接参数：

- `q`：查询关键词
- `le`：语言。英语:`eng`
- `num`：返回数量。
- `ver`：版本号。可为空
- `doctype`：返回类型。`json` 或 `xml`，为空默认 `xml`
- `keyform`：`mdict.` + 版本号 + `.手机平台`。可为空
- `model`：手机型号。可为空
- `mid`：平台版本。可为空
- `imei`：???。可为空
- `vendor`：应用下载平台。可为空
- `screen`：屏幕宽高。可为空
- `ssid`：用户名。可为空
- `abtest`：???。可为空

url 示例：[`http://dict.youdao.com/suggest?q=a&le=eng&num=15&ver=2.0&doctype=json&keyfrom=mdict.7.2.0.android&model=honor&mid=5.6.1&imei=659135764921685&vendor=wandoujia&screen=1080x1800&ssid=superman&abtest=2`](http://dict.youdao.com/suggest?q=a&le=eng&num=15&ver=2.0&doctype=json&keyfrom=mdict.7.2.0.android&model=honor&mid=5.6.1&imei=659135764921685&vendor=wandoujia&screen=1080x1800&ssid=superman&abtest=2) 或 [`http://dict.youdao.com/suggest?q=a&le=eng&num=80&ver=&doctype=json&keyfrom=&model=&mid=&imei=&vendor=&screen=&ssid=&abtest=`](http://dict.youdao.com/suggest?q=a&le=eng&num=80&ver=&doctype=json&keyfrom=&model=&mid=&imei=&vendor=&screen=&ssid=&abtest=)

json 示例：

<h2 id="explain">释义</h2>

url：`http://dict.youdao.com/jsonapi`

拼接参数：

- `jsonversion`：json 版本，目前已知取值`1`或`2`，返回结果大同小异。本文档采用`2`
- `client`：客户端类型，取值`mobile`
- `q`：查询单词
- `dicts`：需要查询哪些字典。目前已知 `{"count":99,"dicts":[["ec","ce","newcj","newjc","kc","ck","fc","cf","multle","jtj","pic_dict","tc","ct","typos","special","tcb","baike","lang","simple","wordform","exam_dict","ctc","web_search","auth_sents_part","ec21","phrs","input","wikipedia_digest","ee","collins","ugc","media_sents_part","syno","rel_word","longman","ce_new","le","newcj_sents","blng_sents_part","hh"],["ugc"],["longman"],["newjc"],["newcj"],["web_trans"],["fanyi"]]}`。可为空，为空则返回全部字段
- `keyfrom`：略，可见[联想](#associate)
- `model`：略，可见[联想](#associate)
- `mid`：略，可见[联想](#associate)
- `imei`：略，可见[联想](#associate)
- `vendor`：略，可见[联想](#associate)
- `screen`：略，可见[联想](#associate)
- `ssid`：略，可见[联想](#associate)
- `network`：网络状态，取值 `wifi`、`4G`、`5G` 等
- `abtest`：略，可见[联想](#associate)
- `xmlVersion`：

url 示例:[`http://dict.youdao.com/jsonapi?jsonversion=2&client=mobile&q=account&dicts=%7B%22count%22%3A99%2C%22dicts%22%3A%5B%5B%22ec%22%2C%22ce%22%2C%22newcj%22%2C%22newjc%22%2C%22kc%22%2C%22ck%22%2C%22fc%22%2C%22cf%22%2C%22multle%22%2C%22jtj%22%2C%22pic_dict%22%2C%22tc%22%2C%22ct%22%2C%22typos%22%2C%22special%22%2C%22tcb%22%2C%22baike%22%2C%22lang%22%2C%22simple%22%2C%22wordform%22%2C%22exam_dict%22%2C%22ctc%22%2C%22web_search%22%2C%22auth_sents_part%22%2C%22ec21%22%2C%22phrs%22%2C%22input%22%2C%22wikipedia_digest%22%2C%22ee%22%2C%22collins%22%2C%22ugc%22%2C%22media_sents_part%22%2C%22syno%22%2C%22rel_word%22%2C%22longman%22%2C%22ce_new%22%2C%22le%22%2C%22newcj_sents%22%2C%22blng_sents_part%22%2C%22hh%22%5D%2C%5B%22ugc%22%5D%2C%5B%22longman%22%5D%2C%5B%22newjc%22%5D%2C%5B%22newcj%22%5D%2C%5B%22web_trans%22%5D%2C%5B%22fanyi%22%5D%5D%7D&keyfrom=mdict.7.2.0.android&model=honor&mid=5.6.1&imei=659135764921685&vendor=wandoujia&screen=1080x1800&ssid=superman&network=wifi&abtest=2&xmlVersion=5.1`](http://dict.youdao.com/jsonapi?jsonversion=2&client=mobile&q=account&dicts=%7B%22count%22%3A99%2C%22dicts%22%3A%5B%5B%22ec%22%2C%22ce%22%2C%22newcj%22%2C%22newjc%22%2C%22kc%22%2C%22ck%22%2C%22fc%22%2C%22cf%22%2C%22multle%22%2C%22jtj%22%2C%22pic_dict%22%2C%22tc%22%2C%22ct%22%2C%22typos%22%2C%22special%22%2C%22tcb%22%2C%22baike%22%2C%22lang%22%2C%22simple%22%2C%22wordform%22%2C%22exam_dict%22%2C%22ctc%22%2C%22web_search%22%2C%22auth_sents_part%22%2C%22ec21%22%2C%22phrs%22%2C%22input%22%2C%22wikipedia_digest%22%2C%22ee%22%2C%22collins%22%2C%22ugc%22%2C%22media_sents_part%22%2C%22syno%22%2C%22rel_word%22%2C%22longman%22%2C%22ce_new%22%2C%22le%22%2C%22newcj_sents%22%2C%22blng_sents_part%22%2C%22hh%22%5D%2C%5B%22ugc%22%5D%2C%5B%22longman%22%5D%2C%5B%22newjc%22%5D%2C%5B%22newcj%22%5D%2C%5B%22web_trans%22%5D%2C%5B%22fanyi%22%5D%5D%7D&keyfrom=mdict.7.2.0.android&model=honor&mid=5.6.1&imei=659135764921685&vendor=wandoujia&screen=1080x1800&ssid=superman&network=wifi&abtest=2&xmlVersion=5.1) 或 [`http://dict.youdao.com/jsonapi?xmlVersion=5.1&client=&q=account&dicts=&keyfrom=&model=&mid=&imei=&vendor=&screen=&ssid=&network=5g&abtest=&jsonversion=2`](http://dict.youdao.com/jsonapi?xmlVersion=5.1&client=&q=account&dicts=&keyfrom=&model=&mid=&imei=&vendor=&screen=&ssid=&network=5g&abtest=&jsonversion=2)

json 示例：

	{
	  "simple": {
	    "query": "account",
	    "word": [
	      {
	        "ukspeech": "account&type=1",
	        "return-phrase": "account",
	        "usspeech": "account&type=2",
	        "usphone": "ə'kaʊnt",
	        "ukphone": "ə'kaʊnt"
	      }
	    ]
	  },
	  "le": "en",
	  "lang": "eng",
	  "input": "account",
	  "ec": {
	    "source": {
	      "name": "有道词典",
	      "url": "http://dict.youdao.com"
	    },
	    "word": [
	      {
	        "trs": [
	          {
	            "tr": [
	              {
	                "l": {
	                  "i": [
	                    "n. 账户；解释；账目，账单；理由；描述"
	                  ]
	                }
	              }
	            ]
	          },
	          {
	            "tr": [
	              {
	                "l": {
	                  "i": [
	                    "vi. 解释；导致；报账"
	                  ]
	                }
	              }
	            ]
	          },
	          {
	            "tr": [
	              {
	                "l": {
	                  "i": [
	                    "vt. 认为；把…视为"
	                  ]
	                }
	              }
	            ]
	          }
	        ],
	        "ukspeech": "account&type=1",
	        "return-phrase": {
	          "l": {
	            "i": "account"
	          }
	        },
	        "usspeech": "account&type=2",
	        "usphone": "ə'kaʊnt",
	        "ukphone": "ə'kaʊnt"
	      }
	    ],
	    "exam_type": [
	      "CET6",
	      "考研",
	      "CET4",
	      "IELTS",
	      "高中",
	      "商务英语",
	      "TOEFL"
	    ]
	  },
	  "special": "",
	  "exam_dict": "",
	  "auth_sents_part": "",
	  "ec21": "",
	  "phrs": "",
	  "wikipedia_digest": "",
	  "ee": "",
	  "collins": "",
	  "ugc": {
	    "data": {
	      "content": "account, （单词解释）英语词语，n.计算， 帐目， 说明， 估计， 理由；vi.说明， 总计有， 认为， 得分；vt.认为。另有会计术语，意为计账户。",
	      "num": 3,
	      "userName": "jrdickso"
	    },
	    "success": true
	  },
	  "media_sents_part": "",
	  "syno": "",
	  "rel_word": "",
	  "longman": {
	    "isGood": "true",
	    "wordList": [
	      {
	        "Entry": {
	          "Sense": [
	            {
	              "EXAMPLETRAN": [
	                "乔姆斯基关于儿童如何学习第一语言的描述"
	              ],
	              "DEF": [
	                "a written or spoken description that says what happens in an event or process"
	              ],
	              "TRAN": [
	                "叙述，描写，报道"
	              ],
	              "SIGNPOST": [
	                "description"
	              ],
	              "GramExa": [
	                {
	                  "EXAMPLETRAN": [
	                    "他因受惊过度而无法描述所发生的事情。"
	                  ],
	                  "PROPFORMPREP": [
	                    "of"
	                  ],
	                  "EXAMPLE": [
	                    "He was too shocked to <i>give an account</i> of what had happened."
	                  ]
	                },
	                {
	                  "PROPFORM": [
	                    "blow-by-blow account"
	                  ],
	                  "EXAMPLETRAN": [
	                    "英格兰队如何负于葡萄牙队的详细报道"
	                  ],
	                  "COLLOTRAN": [
	                    "一五一十的叙述"
	                  ],
	                  "EXAMPLE": [
	                    "a blow-by-blow account of how England lost to Portugal"
	                  ],
	                  "GLOSS": [
	                    "a description of all the details of an event in the order that they happened"
	                  ]
	                },
	                {
	                  "PROPFORM": [
	                    "eye-witness/first-hand account"
	                  ],
	                  "EXAMPLETRAN": [
	                    "目击者讲到平民无故被枪击。",
	                    "这是关于这场战争的第一手报道。"
	                  ],
	                  "COLLOTRAN": [
	                    "目击者的/第一手的描述"
	                  ],
	                  "EXAMPLE": [
	                    "Eye-witness accounts told of the unprovoked shooting of civilians.",
	                    "This gives a first-hand account of the war."
	                  ],
	                  "GLOSS": [
	                    "a description of events by someone who saw them"
	                  ]
	                }
	              ],
	              "EXAMPLE": [
	                "Chomsky’s account of how children learn their first language"
	              ],
	              "SIGNTRAN": [
	                "描述"
	              ]
	            },
	            {
	              "EXAMPLETRAN": [
	                "我的工资直接存入我的银行账户。",
	                "我在巴克莱银行开了一个账户。",
	                "我和丈夫有个联名账户。"
	              ],
	              "DEF": [
	                "an arrangement in which a bank keeps your money safe so that you can pay more in or take money out"
	              ],
	              "Crossref": [
	                {
	                  "Crossrefto": [
	                    {
	                      "REFHWD": [
	                        "bank account"
	                      ]
	                    },
	                    {
	                      "REFHWD": [
	                        "checking account"
	                      ]
	                    },
	                    {
	                      "REFHWD": [
	                        "current account"
	                      ]
	                    },
	                    {
	                      "REFHWD": [
	                        "deposit account"
	                      ]
	                    },
	                    {
	                      "REFHWD": [
	                        "profit and loss account"
	                      ]
	                    },
	                    {
	                      "REFHWD": [
	                        "savings account"
	                      ]
	                    }
	                  ]
	                }
	              ],
	              "TRAN": [
	                "账户"
	              ],
	              "SIGNPOST": [
	                "at a bank"
	              ],
	              "Variant": [
	                {
	                  "LINKWORD": [
	                    "written abbreviation <i>书面缩写为</i>",
	                    "or"
	                  ],
	                  "ABBR": [
	                    "a/c",
	                    "acct."
	                  ]
	                }
	              ],
	              "EXAMPLE": [
	                "My salary is paid into my bank account.",
	                "I’ve <i>opened an account</i> with Barclay’s Bank.",
	                "My husband and I have a <i>joint account</i> (= <em> one that is shared between two people </em> ) ."
	              ],
	              "SIGNTRAN": [
	                "在银行"
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "take account of sth"
	              ],
	              "EXAMPLETRAN": [
	                "这些数字没有把通货膨胀率的变化考虑进去。"
	              ],
	              "DEF": [
	                "to consider or include particular facts or details when making a decision or judgment about something"
	              ],
	              "TRAN": [
	                "考虑到某事，把某事考虑进去"
	              ],
	              "Variant": [
	                {
	                  "LEXVAR": [
	                    "take sth into account"
	                  ],
	                  "LINKWORD": [
	                    "also <i>又作</i>"
	                  ]
	                }
	              ],
	              "EXAMPLE": [
	                "These figures do not take account of changes in the rate of inflation."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "on account of sth"
	              ],
	              "EXAMPLETRAN": [
	                "因为背部有问题，她被建议穿平底鞋。"
	              ],
	              "DEF": [
	                "because of something else, especially a problem or difficulty"
	              ],
	              "TRAN": [
	                "因为某事，由于某事"
	              ],
	              "EXAMPLE": [
	                "She was told to wear flat shoes, on account of her back problem."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "accounts"
	              ],
	              "Subsense": [
	                {
	                  "GRAMTRAN": [
	                    "复数"
	                  ],
	                  "EXAMPLETRAN": [
	                    "去年的账目显示利润为200万美元。"
	                  ],
	                  "DEF": [
	                    "an exact record of the money that a company has received and the money it has spent"
	                  ],
	                  "TRAN": [
	                    "账目"
	                  ],
	                  "GRAM": [
	                    "plural"
	                  ],
	                  "EXAMPLE": [
	                    "The accounts for last year showed a profit of $2 million."
	                  ]
	                },
	                {
	                  "EXAMPLETRAN": [
	                    "艾琳在财务部工作。"
	                  ],
	                  "DEF": [
	                    "a department in a company that is responsible for keeping records of the amount of money spent and received"
	                  ],
	                  "TRAN": [
	                    "〔公司的〕财务部"
	                  ],
	                  "GRAM": [
	                    "U"
	                  ],
	                  "EXAMPLE": [
	                    "Eileen works in accounts."
	                  ]
	                }
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "on account"
	              ],
	              "DEF": [
	                "if you buy goods on account, you take them away with you and pay for them later"
	              ],
	              "TRAN": [
	                "赊账"
	              ]
	            },
	            {
	              "SYN": [
	                "credit account"
	              ],
	              "EXAMPLETRAN": [
	                "你能把这记在我的（赊欠）账上吗？",
	                "一个能无限使用的因特网后付费账户"
	              ],
	              "DEF": [
	                "an arrangement that you have with a shop or company, which allows you to buy goods or use a service now and pay for them later"
	              ],
	              "TRAN": [
	                "〔可先使用后付款的〕赊欠账户"
	              ],
	              "SIGNPOST": [
	                "with a shop/company"
	              ],
	              "EXAMPLE": [
	                "Can you charge this to my account please?",
	                "an unlimited-use Internet account"
	              ],
	              "SIGNTRAN": [
	                "商店/公司"
	              ]
	            },
	            {
	              "SYN": [
	                "bill"
	              ],
	              "DEF": [
	                "a statement that shows how much money you owe for things you have bought from a shop"
	              ],
	              "TRAN": [
	                "账单"
	              ],
	              "SIGNPOST": [
	                "bill"
	              ],
	              "GramExa": [
	                {
	                  "PROPFORM": [
	                    "pay/settle your account"
	                  ],
	                  "EXAMPLETRAN": [
	                    "詹姆斯用信用卡结完账离开餐厅。"
	                  ],
	                  "COLLOTRAN": [
	                    "付账/结账"
	                  ],
	                  "EXAMPLE": [
	                    "James left the restaurant, settling his account by credit card."
	                  ],
	                  "GLOSS": [
	                    "pay what you owe"
	                  ]
	                }
	              ],
	              "SIGNTRAN": [
	                "账单"
	              ]
	            },
	            {
	              "EXAMPLETRAN": [
	                "我们的销售部经理最近拉到了好几笔大生意。"
	              ],
	              "DEF": [
	                "an arrangement to sell goods and services to another company over a period of time"
	              ],
	              "TRAN": [
	                "〔一段时间内的〕交易安排"
	              ],
	              "SIGNPOST": [
	                "arrangement to sell goods"
	              ],
	              "EXAMPLE": [
	                "Our sales manager has secured several big accounts recently."
	              ],
	              "SIGNTRAN": [
	                "售货安排"
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "by/from all accounts"
	              ],
	              "EXAMPLETRAN": [
	                "谁都说这是一桩美满的婚姻。"
	              ],
	              "DEF": [
	                "according to what a lot of people say"
	              ],
	              "TRAN": [
	                "根据各方面所说"
	              ],
	              "EXAMPLE": [
	                "It has, from all accounts, been a successful marriage."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "on sb’s account"
	              ],
	              "EXAMPLETRAN": [
	                "请不要为了我而改变你的计划。"
	              ],
	              "DEF": [
	                "if you do something on someone’s account, you do it because you think they want you to"
	              ],
	              "TRAN": [
	                "为了某人的缘故"
	              ],
	              "EXAMPLE": [
	                "Please don’t change your plans on my account."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "on your own account"
	              ],
	              "EXAMPLETRAN": [
	                "卡丽决定自己做点研究。"
	              ],
	              "DEF": [
	                "by yourself or for yourself"
	              ],
	              "TRAN": [
	                "靠自己；为自己"
	              ],
	              "EXAMPLE": [
	                "Carrie decided to do a little research on her own account."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "on no account/not on any account"
	              ],
	              "EXAMPLETRAN": [
	                "你千万不要打扰我。"
	              ],
	              "DEF": [
	                "used when saying that someone must not, for any reason, do something"
	              ],
	              "TRAN": [
	                "决不，绝对不"
	              ],
	              "EXAMPLE": [
	                "On no account must you disturb me."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "by sb’s own account"
	              ],
	              "EXAMPLETRAN": [
	                "据本特利自己说，他对批评过于敏感。"
	              ],
	              "DEF": [
	                "according to what you have said, especially when you have admitted doing something wrong"
	              ],
	              "TRAN": [
	                "据某人自己所说"
	              ],
	              "EXAMPLE": [
	                "Bentley was, by his own account, over-sensitive to criticism."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "on that account/on this account"
	              ],
	              "EXAMPLETRAN": [
	                "没有必要再为那事担心了。"
	              ],
	              "DEF": [
	                "concerning a particular situation"
	              ],
	              "TRAN": [
	                "由于那个/这个缘故"
	              ],
	              "EXAMPLE": [
	                "There needn’t be any more worries on that account."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "give a good/poor account of yourself"
	              ],
	              "EXAMPLETRAN": [
	                "凯文在今天的比赛中表现出色。"
	              ],
	              "DEF": [
	                "to do something or perform very well or very badly"
	              ],
	              "TRAN": [
	                "表现好/表现差"
	              ],
	              "EXAMPLE": [
	                "Kevin gave a good account of himself in today’s game."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "bring/call sb to account"
	              ],
	              "EXAMPLETRAN": [
	                "这起事故的责任人一直没有被追究责任。"
	              ],
	              "REGISTERLAB": [
	                "formal"
	              ],
	              "DEF": [
	                "to force someone who is responsible for a mistake or a crime to explain publicly why they did it and punish them for it if necessary"
	              ],
	              "LABELTRAN": [
	                "【正式】"
	              ],
	              "TRAN": [
	                "追究某人的责任"
	              ],
	              "EXAMPLE": [
	                "The people responsible for the accident have never been brought to account."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "put/turn sth to good account"
	              ],
	              "EXAMPLETRAN": [
	                "通过帮助我们，也许她可以把自己的某些才能充分发挥出来。"
	              ],
	              "REGISTERLAB": [
	                "formal"
	              ],
	              "DEF": [
	                "to use something for a good purpose"
	              ],
	              "LABELTRAN": [
	                "【正式】"
	              ],
	              "TRAN": [
	                "善用某物，充分利用某物"
	              ],
	              "EXAMPLE": [
	                "Perhaps she could put some of her talents to good account by helping us."
	              ]
	            },
	            {
	              "LEXUNIT": [
	                "of no/little account"
	              ],
	              "EXAMPLETRAN": [
	                "她渐渐长大，父亲对她也不重要了。"
	              ],
	              "REGISTERLAB": [
	                "formal"
	              ],
	              "DEF": [
	                "not important"
	              ],
	              "LABELTRAN": [
	                "【正式】"
	              ],
	              "TRAN": [
	                "不重要，没关系"
	              ],
	              "EXAMPLE": [
	                "As she grew up, her father was of no account to her."
	              ]
	            }
	          ],
	          "Head": [
	            {
	              "HOMNUM": [
	                "1"
	              ],
	              "FREQ": [
	                "S1",
	                "W1"
	              ],
	              "VIDEOCAL": [
	                "http://ydschool-online.nos.netease.com/account_v0205.mp3"
	              ],
	              "PronCodes": [
	                {
	                  "PRONKK": [
	                    "əˋka u nt"
	                  ],
	                  "PRON": [
	                    "əˈkaʊnt"
	                  ]
	                }
	              ],
	              "HWD": [
	                "account"
	              ],
	              "POS": [
	                "n"
	              ],
	              "GRAM": [
	                "C"
	              ],
	              "HYPHENATION": [
	                "ac‧count"
	              ]
	            }
	          ]
	        }
	      },
	      {
	        "Entry": {
	          "Head": [
	            {
	              "HOMNUM": [
	                "2"
	              ],
	              "FREQ": [
	                "S3",
	                "W2"
	              ],
	              "VIDEOCAL": [
	                "http://ydschool-online.nos.netease.com/account_v0205.mp3"
	              ],
	              "HWD": [
	                "account"
	              ],
	              "POS": [
	                "v"
	              ],
	              "HYPHENATION": [
	                "account"
	              ]
	            }
	          ],
	          "PhrVbEntry": [
	            {
	              "Sense": [
	                {
	                  "EXAMPLETRAN": [
	                    "非裔美国人占美国人口的12%。"
	                  ],
	                  "DEF": [
	                    "to form a particular amount or part of something"
	                  ],
	                  "TRAN": [
	                    "占〔一定数量或比例〕"
	                  ],
	                  "EXAMPLE": [
	                    "Afro-Americans account for 12% of the US population."
	                  ]
	                },
	                {
	                  "SYN": [
	                    "explain"
	                  ],
	                  "EXAMPLETRAN": [
	                    "他的行为也许是最近的工作压力导致的。"
	                  ],
	                  "DEF": [
	                    "to be the reason why something happens"
	                  ],
	                  "TRAN": [
	                    "是…的原因"
	                  ],
	                  "EXAMPLE": [
	                    "Recent pressure at work may account for his behavior."
	                  ]
	                },
	                {
	                  "SYN": [
	                    "explain"
	                  ],
	                  "EXAMPLETRAN": [
	                    "你能说明一下你那天晚上的行踪吗？"
	                  ],
	                  "DEF": [
	                    "to give a satisfactory explanation of why something has happened or why you did something"
	                  ],
	                  "TRAN": [
	                    "解释，说明"
	                  ],
	                  "EXAMPLE": [
	                    "Can you account for your movements on that night?"
	                  ]
	                },
	                {
	                  "EXAMPLETRAN": [
	                    "地震发生3天后，仍有150多人下落不明。"
	                  ],
	                  "DEF": [
	                    "to say where all the members of a group of people or things are, especially because you are worried that some of them may be lost"
	                  ],
	                  "TRAN": [
	                    "说明…在何处"
	                  ],
	                  "EXAMPLE": [
	                    "Three days after the earthquake, more than 150 people had still to be accounted for."
	                  ]
	                }
	              ],
	              "Head": [
	                {
	                  "POS": [
	                    "phr v"
	                  ],
	                  "PHRVBHWD": [
	                    "account for <i>sth</i>"
	                  ]
	                }
	              ]
	            }
	          ]
	        }
	      }
	    ]
	  },
	  "blng_sents_part": "",
	  "web_trans": {
	    "web-translation": [
	      {
	        "trans": [
	          {
	            "summary": {
	              "line": [
	                "然而2年下来掐指一算，在中国<b>帐户</b>身上不仅没赚到钱，反而是亏钱，不管若何算，中国<b>帐户</b>(<b>Account</b>)是存得少取得多，全速扑克总觉得吃了大亏，但又的确找不到拒绝支付的理由，于是看见中国<b>帐户</b>提款就封杀，至于理由，自然(Natural..."
	              ]
	            },
	            "support": 731,
	            "value": "帐户",
	            "url": ""
	          },
	          {
	            "summary": {
	              "line": [
	                "我的Neteller<b>账户</b>(<b>Account</b>)是美元<b>账户</b>，只是用来打扑克，但是我的银行<b>账户</b>是欧元<b>账户</b>。Neteller供给了的今天实际汇率，令人绝对吃惊的是，它的汇率是1202。"
	              ]
	            },
	            "support": 726,
	            "value": "账户",
	            "url": ""
	          },
	          {
	            "summary": {
	              "line": [
	                "中文:<b>会计科目</b>;英语:<b>account</b>;日语:勘定科目;韩语:계정;"
	              ]
	            },
	            "support": 541,
	            "value": "会计科目",
	            "url": ""
	          },
	          {
	            "summary": {
	              "line": [
	                "[托业考试]TOEIC词汇汇总(18) ... <b>account </b><b>帐目</b>；帐单；帐户 balance 余额；差额 bond 债券 ..."
	              ]
	            },
	            "support": 470,
	            "value": "帐目",
	            "url": ""
	          }
	        ],
	        "@same": "true",
	        "key-speech": "Account",
	        "key": "Account"
	      },
	      {
	        "trans": [
	          {
	            "value": "帐目编号"
	          },
	          {
	            "value": "帐号"
	          },
	          {
	            "value": "银行帐号"
	          },
	          {
	            "value": "会员帐号"
	          }
	        ],
	        "key-speech": "account+number",
	        "key": "account number"
	      },
	      {
	        "trans": [
	          {
	            "value": "储蓄帐户"
	          },
	          {
	            "value": "有利息"
	          },
	          {
	            "value": "储蓄账户"
	          },
	          {
	            "value": "存款帐户"
	          }
	        ],
	        "key-speech": "saving+account",
	        "key": "saving account"
	      },
	      {
	        "trans": [
	          {
	            "value": "客户经理"
	          },
	          {
	            "value": "客户主任"
	          },
	          {
	            "value": "客户执行"
	          },
	          {
	            "value": "客户代表"
	          }
	        ],
	        "key-speech": "account+executive",
	        "key": "account executive"
	      },
	      {
	        "trans": [
	          {
	            "value": "支票帐户"
	          },
	          {
	            "value": "支票账户"
	          },
	          {
	            "value": "支票"
	          },
	          {
	            "value": "存款支票户"
	          }
	        ],
	        "key-speech": "checking+account",
	        "key": "checking account"
	      },
	      {
	        "trans": [
	          {
	            "value": "存款帐户"
	          },
	          {
	            "value": "定期存款帐户"
	          },
	          {
	            "value": "存款账户"
	          },
	          {
	            "value": "存款账号"
	          }
	        ],
	        "key-speech": "deposit+account",
	        "key": "deposit account"
	      },
	      {
	        "trans": [
	          {
	            "value": "组帐号"
	          },
	          {
	            "value": "集团帐户"
	          },
	          {
	            "value": "集团帐目"
	          },
	          {
	            "value": "组帐户"
	          }
	        ],
	        "key-speech": "group+account",
	        "key": "group account"
	      },
	      {
	        "trans": [
	          {
	            "value": "未决帐项"
	          },
	          {
	            "value": "未清帐目"
	          },
	          {
	            "value": "未清账款"
	          },
	          {
	            "value": "未消帐款"
	          }
	        ],
	        "key-speech": "outstanding+account",
	        "key": "outstanding account"
	      },
	      {
	        "trans": [
	          {
	            "value": "我的帐户"
	          },
	          {
	            "value": "我的账户"
	          },
	          {
	            "value": "可以查看你的下线连接"
	          },
	          {
	            "value": "我的帐号"
	          }
	        ],
	        "key-speech": "My+Account",
	        "key": "My Account"
	      },
	      {
	        "trans": [
	          {
	            "value": "客户代表"
	          },
	          {
	            "value": "企业组"
	          },
	          {
	            "value": "专员"
	          },
	          {
	            "value": "客户管理专员"
	          }
	        ],
	        "key-speech": "Account+Representative",
	        "key": "Account Representative"
	      }
	    ]
	  }
	}

解析：

- `simple`
	- `query`：查询单词
	- `word`
		- `usphone`：美式发音
		- `ukphone`：英式发音

- `ec`
	- `word`
		- `trs`：释义列表
			- `tr`
				- `l`
					- `i`：释义
	- `exam_type`：考查范围

- `ugc`：用户贡献
	- `data`
		- `content`：具体贡献内容
		- `userName`：用户名
- `longman`：朗文当代高级英语辞典内容
	- `wordList`：释义列表
		- `HOMNUM`：
		- `FREQ`：频率，`S1`
		- ``：
		- ``：
		- ``：
- ``：
- ``：
- ``：
- ``：
- ``：
- ``：
- ``：
- ``：
- ``：
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：