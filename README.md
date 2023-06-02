## info about what is contained in the output files

### text files over time
tmsurf.001 (  time        ust        tst        qst         obukh      thls        z0        wthls      wthvs      wqls )  
tmser1.001 (  time      cc     z_cbase    z_ctop_avg  z_ctop_max      zi         we   <<ql>>  <<ql>>_max   w_max   tke     ql_max)  
tmlsm.001 (     time      Qnet        H          LE         G0     tendskin     rs         ra        tskin        cliq      Wl          rssoil     rsveg       Resp       wco2         An    gcco2)  
### text files over height and time (output every 5)
flux1.001 (LEV HEIGHT  PRES  |   WTHL_SUB    WTHL_RES    WTHL_TOT        WQT_SUB      WQT_RES     WQT_TOT   )   
field.001 (LEV  HGHT    PRES    TEMP       TH_L     THETA      TH_V       QT_AV      QL_AV      U       V   CLOUD FRACTION  CS)   
moments.001 (  LEV   HGHT   PRES     THL**2       THV**2         TH**2       QT**2       U*U      V*V     HGHT     W*W     SKEWW     SFS-TKE)  
flux2.001 (LEV HEIGHT  PRES  |    UW_TOT      VW_TOT       UW_SGS      VW_SGS       UW_RES       VW_RES       WTH_TOT       WQ_L       WTHV_SUB     WTHV_RES     WTHV_TOT)  
radstat.001 (LEV RAD_FLX_HGHT  THL_HGHT  LW_UP        LW_DN        SW_UP       SW_DN       TL_LW_TEND   TL_SW_TEND   TL_LS_TEND   TL_TEND)  
budget.001 (LEV HEIGHT   |   TKE        SHEAR      BUOYANCY     TRANSP     PRES_TRSP     DISS      BUDGET      STORAGE      RESID)  
sbbudget.001 (LEV HEIGHT   |   SBTKE     SBSHEAR     BUOYANCY     SBDISS     SBSTORAGE    SBBUDGET   SBRESID    EKM          KH/KM )  

### net cdf files 
profiles.001.nc
(

    dimensions: 
	time = UNLIMITED ;   // (120 currently) 
	zt = 64 ;  
	zm = 64 ;  
	zts = 4 ;  
variables:   
	  
        
    float zt(zt) ;  
		zt:longname = "Vertical displacement of cell centers" ;  
		zt:units = "m" ;  
	  
        
    float zm(zm) ;  
		zm:longname = "Vertical displacement of cell edges" ;  
		zm:units = "m" ;  
	  
        
    float zts(zts) ;  
		zts:longname = "Soil level depth of cell centers" ;  
		zts:units = "m" ;  
	  
        
    float time(time) ;  
		time:longname = "Time" ;  
		time:units = "s" ;  
		time:_FillValue = -999.f ;  
	  
        
    float rhof(time, zt) ;  
		rhof:longname = "Full level slab averaged density" ;  
		rhof:units = "kg/m^3" ;  
		rhof:_FillValue = -999.f ;  
	  
        
    float rhobf(time, zt) ;  
		rhobf:longname = "Full level base-state density" ;  
		rhobf:units = "kg/m^3" ;  
		rhobf:_FillValue = -999.f ;  
	  
        
    float rhobh(time, zm) ;  
		rhobh:longname = "Half level base-state density" ;  
		rhobh:units = "kg/m^3" ;  
		rhobh:_FillValue = -999.f ;  
	  
        
    float presh(time, zt) ;  
		presh:longname = "Pressure at cell center" ;  
		presh:units = "Pa" ;  
		presh:_FillValue = -999.f ;  
	  
        
    float u(time, zt) ;  
		u:longname = "West-East velocity" ;  
		u:units = "m/s" ;  
		u:_FillValue = -999.f ;  
	  
        
    float v(time, zt) ;  
		v:longname = "South-North velocity" ;  
		v:units = "m/s" ;  
		v:_FillValue = -999.f ;  
	  
        
    float thl(time, zt) ;  
		thl:longname = "Liquid water potential temperature" ;  
		thl:units = "K" ;  
		thl:_FillValue = -999.f ;  
	  
        
    float thv(time, zt) ;  
		thv:longname = "Virtual potential temperature" ;  
		thv:units = "K" ;  
		thv:_FillValue = -999.f ;  
	  
        
    float qt(time, zt) ;  
		qt:longname = "Total water specific humidity" ;  
		qt:units = "kg/kg" ;  
		qt:_FillValue = -999.f ;  
	  
        
    float ql(time, zt) ;  
		ql:longname = "Liquid water specific humidity" ;  
		ql:units = "kg/kg" ;  
		ql:_FillValue = -999.f ;  
	  
        
    float wthls(time, zm) ;  
		wthls:longname = "SFS-Theta_l flux" ;  
		wthls:units = "Km/s" ;  
		wthls:_FillValue = -999.f ;  
	  
        
    float wthlr(time, zm) ;  
		wthlr:longname = "Resolved Theta_l flux" ;  
		wthlr:units = "Km/s" ;  
		wthlr:_FillValue = -999.f ;  
	  
        
    float wthlt(time, zm) ;  
		wthlt:longname = "Total Theta_l flux" ;  
		wthlt:units = "Km/s" ;  
		wthlt:_FillValue = -999.f ;  
	  
        
    float wthvs(time, zm) ;  
		wthvs:longname = "SFS-buoyancy flux" ;  
		wthvs:units = "Km/s" ;  
		wthvs:_FillValue = -999.f ;  
	  
        
    float wthvr(time, zm) ;  
		wthvr:longname = "Resolved buoyancy flux" ;  
		wthvr:units = "Km/s" ;  
		wthvr:_FillValue = -999.f ;  
	  
        
    float wthvt(time, zm) ;  
		wthvt:longname = "Total buoyancy flux" ;  
		wthvt:units = "Km/s" ;  
		wthvt:_FillValue = -999.f ;  
	  
        
    float wqts(time, zm) ;  
		wqts:longname = "SFS-moisture flux" ;  
		wqts:units = "kg/kg m/s" ;  
		wqts:_FillValue = -999.f ;  
	  
        
    float wqtr(time, zm) ;  
		wqtr:longname = "Resolved moisture flux" ;  
		wqtr:units = "kg/kg m/s" ;  
		wqtr:_FillValue = -999.f ;  
	  
        
    float wqtt(time, zm) ;  
		wqtt:longname = "Total moisture flux" ;  
		wqtt:units = "kg/kg m/s" ;  
		wqtt:_FillValue = -999.f ;  
	  
        
    float wqls(time, zm) ;  
		wqls:longname = "SFS-liquid water flux" ;  
		wqls:units = "kg/kg m/s" ;  
		wqls:_FillValue = -999.f ;  
	  
        
    float wqlr(time, zm) ;  
		wqlr:longname = "Resolved liquid water flux" ;  
		wqlr:units = "kg/kg m/s" ;  
		wqlr:_FillValue = -999.f ;  
	  
        
    float wqlt(time, zm) ;  
		wqlt:longname = "Total liquid water flux" ;  
		wqlt:units = "kg/kg m/s" ;  
		wqlt:_FillValue = -999.f ;  
	  
        
    float uws(time, zm) ;  
		uws:longname = "SFS-momentum flux (uw)" ;  
		uws:units = "m^2/s^2" ;  
		uws:_FillValue = -999.f ;  
	  
        
    float uwr(time, zm) ;  
		uwr:longname = "Resolved momentum flux (uw)" ;  
		uwr:units = "m^2/s^2" ;  
		uwr:_FillValue = -999.f ;  
	  
        
    float uwt(time, zm) ;  
		uwt:longname = "Total momentum flux (vw)" ;  
		uwt:units = "m^2/s^2" ;  
		uwt:_FillValue = -999.f ;  
	  
        
    float vws(time, zm) ;  
		vws:longname = "SFS-momentum flux (vw)" ;  
		vws:units = "m^2/s^2" ;  
		vws:_FillValue = -999.f ;  
	  
        
    float vwr(time, zm) ;  
		vwr:longname = "Resolved momentum flux (vw)" ;  
		vwr:units = "m^2/s^2" ;  
		vwr:_FillValue = -999.f ;  
	  
        
    float vwt(time, zm) ;  
		vwt:longname = "Total momentum flux (vw)" ;  
		vwt:units = "m^2/s^2" ;  
		vwt:_FillValue = -999.f ;  
	  
        
    float w2s(time, zm) ;  
		w2s:longname = "SFS-TKE" ;  
		w2s:units = "m^2/s^2" ;  
		w2s:_FillValue = -999.f ;  
	  
        
    float w2r(time, zm) ;  
		w2r:longname = "Resolved vertical velocity variance" ;  
		w2r:units = "m^2/s^2" ;  
		w2r:_FillValue = -999.f ;  
	  
        
    float skew(time, zm) ;  
		skew:longname = "vertical velocity skewness" ;  
		skew:units = "-" ;  
		skew:_FillValue = -999.f ;  
	  
        
    float u2r(time, zt) ;  
		u2r:longname = "Resolved horizontal velocity variance (u)" ;  
		u2r:units = "m^2/s^2" ;  
		u2r:_FillValue = -999.f ;  
	  
        
    float v2r(time, zt) ;  
		v2r:longname = "Resolved horizontal velocity variance (v)" ;  
		v2r:units = "m^2/s^2" ;  
		v2r:_FillValue = -999.f ;  
	  
        
    float thl2r(time, zt) ;  
		thl2r:longname = "Resolved theta_l variance" ;  
		thl2r:units = "K^2" ;  
		thl2r:_FillValue = -999.f ;  
	  
        
    float thv2r(time, zt) ;  
		thv2r:longname = "Resolved buoyancy variance" ;  
		thv2r:units = "K^2" ;  
		thv2r:_FillValue = -999.f ;  
	  
        
    float th2r(time, zt) ;  
		th2r:longname = "Resolved theta variance" ;  
		th2r:units = "K^2" ;  
		th2r:_FillValue = -999.f ;  
	  
        
    float qt2r(time, zt) ;  
		qt2r:longname = "Resolved total water variance" ;  
		qt2r:units = "(kg/kg)^2" ;  
		qt2r:_FillValue = -999.f ;  
	  
        
    float ql2r(time, zt) ;  
		ql2r:longname = "Resolved liquid water variance" ;  
		ql2r:units = "(kg/kg)^2" ;  
		ql2r:_FillValue = -999.f ;  
	  
        
    float cs(time, zt) ;  
		cs:longname = "Smagorinsky constant" ;  
		cs:units = "-" ;  
		cs:_FillValue = -999.f ;  
	  
        
    float thltend(time, zt) ;  
		thltend:longname = "Total radiative tendency" ;  
		thltend:units = "K/s" ;  
		thltend:_FillValue = -999.f ;  
	  
        
    float thllwtend(time, zt) ;  
		thllwtend:longname = "Long wave radiative tendency" ;  
		thllwtend:units = "K/s" ;  
		thllwtend:_FillValue = -999.f ;  
	  
        
    float thlswtend(time, zt) ;  
		thlswtend:longname = "Short wave radiative tendency" ;  
		thlswtend:units = "K/s" ;  
		thlswtend:_FillValue = -999.f ;  
	  
        
    float thlradls(time, zt) ;  
		thlradls:longname = "Large scale radiative tendency" ;  
		thlradls:units = "K/s" ;  
		thlradls:_FillValue = -999.f ;  
	  
        
    float lwu(time, zm) ;  
		lwu:longname = "Long wave upward radiative flux" ;  
		lwu:units = "W/m^2" ;  
		lwu:_FillValue = -999.f ;  
	  
        
    float lwd(time, zm) ;  
		lwd:longname = "Long wave downward radiative flux" ;  
		lwd:units = "W/m^2" ;  
		lwd:_FillValue = -999.f ;  
	  
        
    float swu(time, zm) ;  
		swu:longname = "Short wave upward radiative flux" ;  
		swu:units = "W/m^2" ;  
		swu:_FillValue = -999.f ;  
	  
        
    float swd(time, zm) ;  
		swd:longname = "Short wave downward radiative flux" ;  
		swd:units = "W/m^2" ;  
		swd:_FillValue = -999.f ;  
	  
        
    float lwuca(time, zm) ;  
		lwuca:longname = "Long wave clear air upward radiative flux" ;  
		lwuca:units = "W/m^2" ;  
		lwuca:_FillValue = -999.f ;  
	  
        
    float lwdca(time, zm) ;  
		lwdca:longname = "Long wave clear air downward radiative flux" ;  
		lwdca:units = "W/m^2" ;  
		lwdca:_FillValue = -999.f ;  
	  
        
    float swuca(time, zm) ;  
		swuca:longname = "Short wave clear air upward radiative flux" ;  
		swuca:units = "W/m^2" ;  
		swuca:_FillValue = -999.f ;  
	  
        
    float swdca(time, zm) ;  
		swdca:longname = "Short wave clear air downward radiative flux" ;  
		swdca:units = "W/m^2" ;  
		swdca:_FillValue = -999.f ;  
	  
        
    float tker(time, zt) ;  
		tker:longname = "Resolved TKE" ;  
		tker:units = "m/s^2" ;  
		tker:_FillValue = -999.f ;  
	  
        
    float shr(time, zt) ;  
		shr:longname = "Resolved Shear" ;  
		shr:units = "m/s^2" ;  
		shr:_FillValue = -999.f ;  
	  
        
    float buo(time, zt) ;  
		buo:longname = "Resolved Buoyancy" ;  
		buo:units = "m/s^2" ;  
		buo:_FillValue = -999.f ;  
	  
        
    float trsp(time, zt) ;  
		trsp:longname = "Resolved Transport" ;  
		trsp:units = "m/s^2" ;  
		trsp:_FillValue = -999.f ;  
	  
        
    float ptrsp(time, zt) ;  
		ptrsp:longname = "Resolved Pressure transport (redistribution)" ;  
		ptrsp:units = "m/s^2" ;  
		ptrsp:_FillValue = -999.f ;  
	  
        
    float diss(time, zt) ;  
		diss:longname = "Resolved Dissipation" ;  
		diss:units = "m/s^2" ;  
		diss:_FillValue = -999.f ;  
	  
        
    float budg(time, zt) ;  
		budg:longname = "Resolved Storage = dE/dt" ;  
		budg:units = "m/s^2" ;  
		budg:_FillValue = -999.f ;  
	  
        
    float stor(time, zt) ;  
		stor:longname = "Resolved Budget = sum of contributions excl storage" ;  
		stor:units = "m/s^2" ;  
		stor:_FillValue = -999.f ;  
	  
        
    float resid(time, zt) ;  
		resid:longname = "Resolved Residual = budget - storage" ;  
		resid:units = "m/s^2" ;  
		resid:_FillValue = -999.f ;  
	  
        
    float sbtke(time, zt) ;  
		sbtke:longname = "Subgrid TKE" ;  
		sbtke:units = "m/s^2" ;  
		sbtke:_FillValue = -999.f ;  
	  
        
    float sbshr(time, zt) ;  
		sbshr:longname = "Subgrid Shear" ;  
		sbshr:units = "m/s^2" ;  
		sbshr:_FillValue = -999.f ;  
	  
        
    float sbbuo(time, zt) ;  
		sbbuo:longname = "Subgrid Buoyancy" ;  
		sbbuo:units = "m/s^2" ;  
		sbbuo:_FillValue = -999.f ;  
	  
        
    float sbdiss(time, zt) ;  
		sbdiss:longname = "Subgrid Dissipation" ;  
		sbdiss:units = "m/s^2" ;  
		sbdiss:_FillValue = -999.f ;  
	  
        
    float sbstor(time, zt) ;  
		sbstor:longname = "Subgrid Storage = dE/dt" ;  
		sbstor:units = "m/s^2" ;  
		sbstor:_FillValue = -999.f ;  
	  
        
    float sbbudg(time, zt) ;  
		sbbudg:longname = "Subgrid Budget = sum of contributions excl storage" ;  
		sbbudg:units = "m/s^2" ;  
		sbbudg:_FillValue = -999.f ;  
	  
        
    float sbresid(time, zt) ;  
		sbresid:longname = "Subgrid Residual = budget - storage" ;  
		sbresid:units = "m/s^2" ;  
		sbresid:_FillValue = -999.f ;  
	  
        
    float ekm(time, zt) ;  
		ekm:longname = "Turbulent exchange coefficient momentum" ;  
		ekm:units = "m/s^2" ;  
		ekm:_FillValue = -999.f ;  
	  
        
    float khkm(time, zt) ;  
		khkm:longname = "Kh / Km, in post-processing used to determine filter-grid ratio" ;  
		khkm:units = "m/s^2" ;  
		khkm:_FillValue = -999.f ;  


)
tmser.001.nc
(
    dimensions:   
	time = UNLIMITED ;   // (600 currently)
variables:   
	  
        
    float time(time) ;  
		time:longname = "Time" ;  
		time:units = "s" ;  
		time:_FillValue = -999.f ;  
	  
        
    float cfrac(time) ;  
		cfrac:longname = "Cloud fraction" ;  
		cfrac:units = "-" ;  
		cfrac:_FillValue = -999.f ;  
	  
        
    float zb(time) ;  
		zb:longname = "Cloud-base height" ;  
		zb:units = "m" ;  
		zb:_FillValue = -999.f ;  
	  
        
    float zc_av(time) ;  
		zc_av:longname = "Average Cloud-top height" ;  
		zc_av:units = "m" ;  
		zc_av:_FillValue = -999.f ;  
	  
        
    float zc_max(time) ;  
		zc_max:longname = "Maximum Cloud-top height" ;  
		zc_max:units = "m" ;  
		zc_max:_FillValue = -999.f ;  
	  
        
    float zi(time) ;  
		zi:longname = "Boundary layer height" ;  
		zi:units = "m" ;  
		zi:_FillValue = -999.f ;  
	  
        
    float we(time) ;  
		we:longname = "Entrainment velocity" ;  
		we:units = "m/s" ;  
		we:_FillValue = -999.f ;  
	  
        
    float lwp_bar(time) ;  
		lwp_bar:longname = "Liquid-water path" ;  
		lwp_bar:units = "kg/m^2" ;  
		lwp_bar:_FillValue = -999.f ;  
	  
        
    float lwp_max(time) ;  
		lwp_max:longname = "Maximum Liquid-water path" ;  
		lwp_max:units = "kg/m^2" ;  
		lwp_max:_FillValue = -999.f ;  
	  
        
    float wmax(time) ;  
		wmax:longname = "Maximum vertical velocity" ;  
		wmax:units = "m/s" ;  
		wmax:_FillValue = -999.f ;  
	  
        
    float vtke(time) ;  
		vtke:longname = "Vertical integral of total TKE" ;  
		vtke:units = "kg/s" ;  
		vtke:_FillValue = -999.f ;  
	  
        
    float lmax(time) ;  
		lmax:longname = "Maximum liquid water specific humidity" ;  
		lmax:units = "kg/kg" ;  
		lmax:_FillValue = -999.f ;  
	  
        
    float ustar(time) ;  
		ustar:longname = "Surface friction velocity" ;  
		ustar:units = "m/s" ;  
		ustar:_FillValue = -999.f ;  
	  
        
    float tstr(time) ;  
		tstr:longname = "Turbulent temperature scale" ;  
		tstr:units = "K" ;  
		tstr:_FillValue = -999.f ;  
	  
        
    float qtstr(time) ;  
		qtstr:longname = "Turbulent humidity scale" ;  
		qtstr:units = "K" ;  
		qtstr:_FillValue = -999.f ;  
	  
        
    float obukh(time) ;  
		obukh:longname = "Obukhov Length" ;  
		obukh:units = "m" ;  
		obukh:_FillValue = -999.f ;  
	  
        
    float thlskin(time) ;  
		thlskin:longname = "Surface liquid water potential temperature" ;  
		thlskin:units = "K" ;  
		thlskin:_FillValue = -999.f ;  
	  
        
    float z0(time) ;  
		z0:longname = "Roughness height" ;  
		z0:units = "m" ;  
		z0:_FillValue = -999.f ;  
	  
        
    float wtheta(time) ;  
		wtheta:longname = "Surface kinematic temperature flux" ;  
		wtheta:units = "K m/s" ;  
		wtheta:_FillValue = -999.f ;  
	  
        
    float wthetav(time) ;  
		wthetav:longname = "Surface kinematic virtual temperature flux" ;  
		wthetav:units = "K m/s" ;  
		wthetav:_FillValue = -999.f ;  
	  
        
    float wq(time) ;  
		wq:longname = "Surface kinematic moisture flux" ;  
		wq:units = "kg/kg m/s" ;  
		wq:_FillValue = -999.f ;  
	  
        
    float twp_bar(time) ;  
		twp_bar:longname = "Total water path" ;  
		twp_bar:units = "kg/m^2" ;  
		twp_bar:_FillValue = -999.f ;  
	  
        
    float rwp_bar(time) ;  
		rwp_bar:longname = "Rain water path" ;  
		rwp_bar:units = "kg/m^2" ;  
		rwp_bar:_FillValue = -999.f ;  
	  
        
    float Qnet(time) ;  
		Qnet:longname = "Net radiation" ;  
		Qnet:units = "W/m^2" ;  
		Qnet:_FillValue = -999.f ;  
	  
        
    float H(time) ;  
		H:longname = "Sensible heat flux" ;  
		H:units = "W/m^2" ;  
		H:_FillValue = -999.f ;  
	  
        
    float LE(time) ;  
		LE:longname = "Latent heat flux" ;  
		LE:units = "W/m^2" ;  
		LE:_FillValue = -999.f ;  
	  
        
    float G0(time) ;  
		G0:longname = "Ground heat flux" ;  
		G0:units = "W/m^2" ;  
		G0:_FillValue = -999.f ;  
	  
        
    float tendskin(time) ;  
		tendskin:longname = "Skin tendency" ;  
		tendskin:units = "W/m^2" ;  
		tendskin:_FillValue = -999.f ;  
	  
        
    float rs(time) ;  
		rs:longname = "Surface resistance" ;  
		rs:units = "s/m" ;  
		rs:_FillValue = -999.f ;  
	  
        
    float ra(time) ;  
		ra:longname = "Aerodynamic resistance" ;  
		ra:units = "s/m" ;  
		ra:_FillValue = -999.f ;  
	  
        
    float cliq(time) ;  
		cliq:longname = "Fraction of vegetated surface covered with liquid water" ;  
		cliq:units = "-" ;  
		cliq:_FillValue = -999.f ;  
	  
        
    float Wl(time) ;  
		Wl:longname = "Liquid water reservoir" ;  
		Wl:units = "m" ;  
		Wl:_FillValue = -999.f ;  
	  
        
    float rssoil(time) ;  
		rssoil:longname = "Soil evaporation resistance" ;  
		rssoil:units = "s/m" ;  
		rssoil:_FillValue = -999.f ;  
	  
        
    float rsveg(time) ;  
		rsveg:longname = "Vegitation resistance" ;  
		rsveg:units = "s/m" ;  
		rsveg:_FillValue = -999.f ;  

)
