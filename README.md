
    var banner: GADBannerView!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        loadbanner()
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }


    func loadbanner(){
        banner = GADBannerView(adSize: kGADAdSizeSmartBannerPortrait)
        self.banner.adUnitID = "ca-app-pub-2809593728729827/4252369390"
        self.banner.rootViewController = self
        let requestad: GADRequest = GADRequest()
        self.banner.loadRequest(requestad)
        banner.frame = CGRectMake(0, view.bounds.height - banner.frame.size.height, banner.frame.size.width, banner.frame.size.height)
        self.view.addSubview(banner)
    }

    
}

