# arm32_base_loc
A tool to locate the base address of arm32-little-end firmware binary.  ##ARM固件加载基址定位

使用原程序的python load dll不能正常工作。

直接使用C源代码:
int main()

{
	// (char *filename, int wnd, int gap, float T, unsigned int f_gap_m, int f_rough, unsigned int boot, int f_clear){

	int wnd = 3;
	int gap = 3;
	float T = 0.6;
	unsigned int f_gap_m = 4096;
	int f_rough = 0;
	unsigned int boot = 0x80F36D5;
	int f_clear = 1;
	find_load_base("XXX.bin", wnd, gap, T, f_gap_m, f_rough, boot, f_clear);
}
就能正常工作了.
