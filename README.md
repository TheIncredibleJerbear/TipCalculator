# TipCalculator
import UIKit


class ViewController: UIViewController{
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
    }

    @IBOutlet weak var BillAmountlabel: UILabel!
    @IBOutlet weak var BillAmounttextfeild: UITextField!
    @IBOutlet var TipAmountlabel: UIView!
    @IBOutlet weak var tenpercentlabel: UILabel!
    @IBOutlet weak var fifteenpercentlabel: UILabel!
    @IBOutlet weak var twentypercentlabel: UILabel!
    @IBAction func calculatebutton(_ sender: Any)
   {
        //WILLIAM FIGUERO'S CODE REFERENCE
        if let finalamount = BillAmounttextfeild.text
        {
        let billtotal = Double(finalamount) ?? 0
            print(billtotal)
        //WILLIAM FIGUERO'S REFERENCE
            
            //CALCULATION
            let tenpercentcalculation = String(format: "%.2f",billtotal * 0.10)
            let fifteenpercentcalculation = String(format: "%.2f",billtotal * 0.15)
            let twentypercentcalculation = String(format: "%.2f", billtotal * 0.20)
            
            //DISPLAY
            tenpercentlabel.text = "Your 10 Percent tip is $ \(tenpercentcalculation)"
            fifteenpercentlabel.text = "Your 15 Percent tip is $ \(fifteenpercentcalculation)"
            twentypercentlabel.text = "Your 20 Percent tip is $\(twentypercentcalculation)"
        
        }
        
    }

}
