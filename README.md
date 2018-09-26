# YuvLib
package com.xubaipei.yuv;

/**
 * Created by xubp on 2018/8/23.
 */

public class YuvUtil {
    static {
        System.loadLibrary("yuv_jni");
    }

    /**
     *
     * @param width 宽度
     * @param height 高度
     * @param degree 旋转角度 90 180 270
     * @param input 输入数据
     * @param output 输出数据
     */
    public static native void rotateYuv420sp(int width,int height,int degree,byte[] input,byte[] output);

    /**
     *
     * @param width 宽度
     * @param height 高度
     * @param dir 镜像方向 0:y 轴镜像；1:x轴镜像；2中心轴对称
     * @param input 输入数据
     * @param output 输出数据
     */
    public static native void mirrorYuv420sp(int width,int height,int dir,byte[] input,byte[] output);

    /**
     *@funcion nv21 与 nv 12 相互转换
     * @param width 宽度
     * @param height 高度
     * @param input 输入数据
     * @param output 输出数据
     */
    public static native void Nv21_Nv12(int width,int height,byte[] input,byte[] output);

}
