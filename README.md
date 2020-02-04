#退款接口对接
##C端
###url http://测试环境:9021/charter/refund/create
### 入参
{"businessType":2,"orderId":"15807845749317589","refundReasonExplain":"不想要了22","refundReasonType":1,"refundType":1,"travelIds":[949,950],"custId":"1912058270543763"} 

    @ApiModelProperty(value = "订单编号")
    private String orderId;
    @ApiModelProperty(value = "行程编号")
    private List<Integer> travelIds;


    /**
     * 退款类型，1-App退款 2-后台退款 3需求测退款
     */
    @ApiModelProperty(value = "退款类型")
    private Integer refundType;

    /**
     * 退款原因类型，1-购票退款 2-改签费退款 99其他
     */
    @ApiModelProperty(value = "退款原因类型")
    private Integer refundReasonType;

    /**
     * 退款原因说明
     */
    @ApiModelProperty(value = "退款原因说明")
    private String refundReasonExplain;

    /**
     * 业务类型:1-通勤 2-专线 3-拼车 4-包车 5-企业通勤 6-企业包车
     */
    @ApiModelProperty(value = "业务类型")
    private Integer businessType;

    /**
     * 用户的id
     */
    private String  custId ;
    
### 返回参数
{"data":null,"code":"000000","msg":null,"success":true} 

    @ApiModelProperty(value = "数据",example = "")
    private T data ;

    @ApiModelProperty(value = "响应码",example = "00000000")
    private String code;

    @ApiModelProperty(value = "消息",example = "成功")
    private String msg;

    @ApiModelProperty(value = "是否成功",example = "true")
    private Boolean success;
    
    
##B端（目前可以调用相同的地址）
   
