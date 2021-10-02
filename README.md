# solidity

// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7;

contract fixarray{
    uint[3] public uarray=[1,2,3];
    uint public a=3;
    
   // bytes2[3] byarray=[0x6a6f,0x6f6a,0x5f3a]; error!
   
   bytes2[3] public byarray;
   
   function initbyarray()public returns(bytes2[3] memory){
       byarray[0]=0x6a6f;
       byarray[1]=0x6a6f;
       byarray[2]=0x6a6f;
       return byarray;//不能显示
      
   }
   
   function getbyarray() public view returns(bytes2[3] memory){
       return byarray; //为什么这里可以返回显示bytes数组，初始化那里不能显示
   }
   
   }
