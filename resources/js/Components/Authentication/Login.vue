<template>
    <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bg-gray-100">
        <!--Logo-->
        <div class="flex">
            <slot name="logo"/>
        </div>
        <!--Login form-->
        <div class="w-full sm:max-w-md mt-6 px-6 py-4 bg-white shadow-md overflow-hidden sm:rounded-lg">
            <!--Content-->
            <slot/>
            <!--Language selection-->
<!--            <div class="flex justify-around pt-2 mt-2 -mb-2 border-t">
                &lt;!&ndash;Turkish&ndash;&gt;
                <button class="py-2 justify-center flex-1 hover:bg-blue-200"
                        onclick="window.location.href='http://laraquality/dil/tr'">
                    <svg class="inline-block rounded-full w-8 h-8 mr-2" viewBox="0 0 512 512"
                         xmlns="http://www.w3.org/2000/svg">
                        <circle cx="256" cy="256" r="256" style="fill:#D80027;"></circle>
                        <g style="" transform="matrix(1.545738, 0, 0, 1.544734, -23.607437, -142.003983)">
                            <polygon points="245.518,209.186 266.523,238.131 300.54,227.101 279.502,256.021 300.504,284.965
		266.499,273.893 245.462,302.813 245.484,267.052 211.478,255.98 245.496,244.95 	"
                                     style="fill:#F0F0F0;"></polygon>
                            <path
                                d="M188.194,328.348c-39.956,0-72.348-32.392-72.348-72.348s32.392-72.348,72.348-72.348 c12.458,0,24.18,3.151,34.414,8.696c-16.055-15.702-38.012-25.392-62.24-25.392c-49.178,0-89.043,39.866-89.043,89.043 s39.866,89.043,89.043,89.043c24.23,0,46.186-9.691,62.24-25.392C212.374,325.197,200.652,328.348,188.194,328.348z"
                                style="fill:#F0F0F0;"></path>
                        </g>
                    </svg>
                    Türkçe
                </button>
                &lt;!&ndash;English&ndash;&gt;
                <button class="py-2 justify-center flex-1 hover:bg-blue-200"
                        onclick="window.location.href='http://laraquality/dil/en'">
                    <svg id="Layer_1" class="inline-block rounded-full w-8 h-8 mr-2"
                         style="" version="1.1" viewBox="0 0 512 512" x="0px" xml:space="preserve"
                         xmlns="http://www.w3.org/2000/svg"
                         xmlns:xlink="http://www.w3.org/1999/xlink" y="0px">
                                    <circle cx="256" cy="256" r="256" style="fill:#F0F0F0;"></circle>
                        <g>
        <path d="M52.92,100.142c-20.109,26.163-35.272,56.318-44.101,89.077h133.178L52.92,100.142z"
              style="fill:#0052B4;"></path>
                            <path d="M503.181,189.219c-8.829-32.758-23.993-62.913-44.101-89.076l-89.075,89.076H503.181z"
                                  style="fill:#0052B4;"></path>
                            <path
                                d="M8.819,322.784c8.83,32.758,23.993,62.913,44.101,89.075l89.074-89.075L8.819,322.784L8.819,322.784   z"
                                style="fill:#0052B4;"></path>
                            <path d="M411.858,52.921c-26.163-20.109-56.317-35.272-89.076-44.102v133.177L411.858,52.921z"
                                  style="fill:#0052B4;"></path>
                            <path
                                d="M100.142,459.079c26.163,20.109,56.318,35.272,89.076,44.102V370.005L100.142,459.079z"
                                style="fill:#0052B4;"></path>
                            <path d="M189.217,8.819c-32.758,8.83-62.913,23.993-89.075,44.101l89.075,89.075V8.819z"
                                  style="fill:#0052B4;"></path>
                            <path d="M322.783,503.181c32.758-8.83,62.913-23.993,89.075-44.101l-89.075-89.075V503.181z"
                                  style="fill:#0052B4;"></path>
                            <path d="M370.005,322.784l89.075,89.076c20.108-26.162,35.272-56.318,44.101-89.076H370.005z"
                                  style="fill:#0052B4;"></path>
    </g>
                        <g>
        <path
            d="M509.833,222.609h-220.44h-0.001V2.167C278.461,0.744,267.317,0,256,0   c-11.319,0-22.461,0.744-33.391,2.167v220.44v0.001H2.167C0.744,233.539,0,244.683,0,256c0,11.319,0.744,22.461,2.167,33.391   h220.44h0.001v220.442C233.539,511.256,244.681,512,256,512c11.317,0,22.461-0.743,33.391-2.167v-220.44v-0.001h220.442   C511.256,278.461,512,267.319,512,256C512,244.683,511.256,233.539,509.833,222.609z"
            style="fill:#D80027;"></path>
                            <path
                                d="M322.783,322.784L322.783,322.784L437.019,437.02c5.254-5.252,10.266-10.743,15.048-16.435   l-97.802-97.802h-31.482V322.784z"
                                style="fill:#D80027;"></path>
                            <path
                                d="M189.217,322.784h-0.002L74.98,437.019c5.252,5.254,10.743,10.266,16.435,15.048l97.802-97.804   V322.784z"
                                style="fill:#D80027;"></path>
                            <path
                                d="M189.217,189.219v-0.002L74.981,74.98c-5.254,5.252-10.266,10.743-15.048,16.435l97.803,97.803   H189.217z"
                                style="fill:#D80027;"></path>
                            <path
                                d="M322.783,189.219L322.783,189.219L437.02,74.981c-5.252-5.254-10.743-10.266-16.435-15.047   l-97.802,97.803V189.219z"
                                style="fill:#D80027;"></path>
    </g>
</svg>
                    English
                </button>
            </div>-->
        </div>
    </div>
</template>
