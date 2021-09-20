# Rangkuman Pertemuan 3

1.	Pertama menguji coba membuat kelas temperature untuk konversi unit dengan cara menghapus semua file di org.aplas.basiappx test kemudian membuat kelas temperature baru difolder yang sama pada main activity selanjutnya membuat private field serta parameter : 
public class Temperature {
    private double celcius;
    private double fahrenheit;
    private double kelvin;

    public Temperature(){
        this.celcius = 0;
    }
    public void setCelcius(double celcius){
        this.celcius = celcius;
    }
    public void setFahrenheit(double fahrenheit){
        this.celcius = (fahrenheit-32)/9*5;
    }
    public void setKelvins(double kelvin){
        this.celcius = kelvin-273.15;
    }
    public double getCelcius(){
        return this.celcius;
    }
    public double getFahrenheit(){
        return celcius*9/5 + 32;
    }
    public double getKelvins(){
        return celcius + 273.15;
    }
    public double convert(String oriUnit, String convUnit, double value){
        if (oriUnit.equals("°C")) {
            setCelcius(value);
        } else if (oriUnit.equals("°F")) {
            setFahrenheit(value);
        } else {
            setKelvins(value);
        }
        if (convUnit.equals("°C")) {
            return getCelcius();
        } else if (convUnit.equals("°F")) {
            return  getFahrenheit();
        } else {
            return getKelvins();
        }
    }

setelah itu mengcopy paste  file java testB1basicactivity011 dan viewtest ke folder org.aplas.basicappx (test) untuk dijalankan projeknya.
2.	Kemudian menguji coba kelas untuk mengkonversi antara kelas distance dengan spesifikasi yang dibutuhkan kemudian membuuat file baru  kelas distance pada projek basicappx di folder org.aplas.basicappx. Setelah itu membuta private field dengan nama meter dan membuat tipe data double untuk membuat konstruktor parameter. Kemudian membuat 4 fungsi untuk memasukan meter pada formula setelah itu membuat fungsi konversi yang berfungsi untuk mengembalikan jumlah konversi dari unit ke salah satu konversi yang sudah Kembali jumlahnya.
public class Distance {
    private double meter;
    private double inch;
    private double mile;
    private double foot;

    public Distance(){
        this.meter = 0;
    }

    public void setMeter(double meter) {
        this.meter = meter;
    }

    public void setInch(double inch) {
        this.meter = inch/39.3701;
    }

    public void setMile(double mile) {
        this.meter = mile/0.000621371;
    }

    public void setFoot(double foot) {
        this.meter = foot/3.28084;
    }

    public double getMeter() {
        return meter;
    }

    public double getInch() {
        return meter*39.3701;
    }

    public double getMile() {
        return meter*0.000621371;
    }

    public double getFoot() {
        return meter*3.28084;
    }

    public double convert (String oriUnit, String convUnit, double value) {
        if (oriUnit.equals("Mtr")) {
            setMeter(value);
        } else if (oriUnit.equals("Inc")) {
            setInch(value);
        } else if (oriUnit.equals("Mil")) {
            setMile(value);
        } else {
            setFoot(value);
        }
        if (convUnit.equals("Mtr")) {
            return getMeter();
        } else if (convUnit.equals("Inc")) {
            return getInch();
        } else if (convUnit.equals("Mil")) {
            return  getMile();
        } else {
            return getFoot();
        }
    }

 setelah itu mengcopy paste  file java testB1basicactivity021 ke folder org.aplas.basicappx untuk dijalankan projeknya.
3.	Membuat dan menguji coba kelas konversi berat pada projek. Pertama membuat file baru kelas berat (weight) di folder org.aplas.basicappx setelah itu membuat private field dengan satuan gram dan tipe datanya dengan konstruktor parameter serta 3 set fungsi untuk memasukkan berat gram ke dalam formula. setelah itu membuat fungsi konversi berat yang berfungsi untuk mengembalikan jumlah konversi dari unit ke salah satu konversi yang sudah Kembali jumlahnya.
public class Weight {
    private double gram;
    private double ounce;
    private double pound;

    public Weight(){
        this.gram = 0;
    }

    public void setGram(double gram) {
        this.gram = gram;
    }

    public void setOunce(double ounce) {
        this.gram = ounce*28.3495231;
    }

    public void setPound(double pound) {
        this.gram = pound*453.59237;
    }

    public double getGram() {
        return gram;
    }

    public double getOunce() {
        return gram/28.3495231;
    }

    public double getPound() {
        return gram/453.59237;
    }

    public double convert (String oriUnit, String convUnit, double value) {
        if (oriUnit.equals("Grm")) {
            setGram(value);
        } else if (oriUnit.equals("Onc")) {
            setOunce(value);
        } else {
            setPound(value);
        }
        if (convUnit.equals("Grm")) {
            return getGram();
        } else if (convUnit.equals("Onc")) {
            return  getOunce();
        } else {
            return getPound();
        }
    }

 setelah itu mengcopy paste  file java testB1basicactivity031 ke folder org.aplas.basicappx untuk dijalankan projeknya.
4.	Mencoba untuk mendefinisikan field dan fungsi pada kelas main activity. Selanjutnya membuka projek basicappx dan main activity untuk membuat  2 fungsi blank dan beberapa field pada main activity :
private Distance dist = new Distance();
private Weight weight = new Weight();
private Temperature temp = new Temperature();

private Button convertBtn;
private EditText inputTxt;
private EditText outputTxt;
private Spinner unitOri;
private Spinner unitConv;
private RadioGroup unitType;
private CheckBox roundBox;
private CheckBox formBox;
private ImageView imgView;
private AlertDialog startDialog;

protected double convertUnit(String type, String oriUnit, String convUnit, double value) {
    if (type.equals("Temperature")) {
        return temp.convert(oriUnit, convUnit, value);
    } else if (type.equals("Distance")) {
        return dist.convert(oriUnit, convUnit, value);
    } else {
        return weight.convert(oriUnit, convUnit, value);
    }
}

protected String strResult(double val, boolean rounded) {
    if (rounded) {
        DecimalFormat f = new DecimalFormat("#.##");
        return f.format(val);
    } else {
        DecimalFormat f = new DecimalFormat("#.#####");
        return f.format(val);
    }
}
Setelah itu membuat fungsi konversi convertUnit bertipe data double dan terdapat 4 parameter yang berfungsi untuk mengembalikan jumlah konversi dari unit ke salah satu konversi dikelas temperature, jarak (distance), dan berat (weight) untuk membuat algoritma pada fungsi konversi tersebut. Serta  membuat fungsi bertipe data string untuk mengembalikan jumlah dobel pada parameter.
protected double convertUnit(String type, String oriUnit, String convUnit, double value) {
    if (type.equals("Temperature")) {
        return temp.convert(oriUnit, convUnit, value);
    } else if (type.equals("Distance")) {
        return dist.convert(oriUnit, convUnit, value);
    } else {
        return weight.convert(oriUnit, convUnit, value);
    }
}

protected String strResult(double val, boolean rounded) {
    if (rounded) {
        DecimalFormat f = new DecimalFormat("#.##");
        return f.format(val);
    } else {
        DecimalFormat f = new DecimalFormat("#.#####");
        return f.format(val);
    }
}
Selanjutnya mengcopy paste  file java testB1basicactivity041 ke folder org.aplas.basicappx untuk dijalankan projeknya.
5.	Pada tahap ini masih sama menambahkan fungsi pada main activity yaitu membuat fungsi onCreate dan onStart yang terdapat pada layout resource serta dibawahnya terdapat private field dengan nama startDialog dan bertipe data AlertDialog.
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    convertBtn = (Button) findViewById(R.id.convertButton);
    inputTxt = (EditText) findViewById(R.id.inputText);
    outputTxt = (EditText) findViewById(R.id.outputText);
    unitOri = (Spinner) findViewById(R.id.oriList);
    unitConv = (Spinner) findViewById(R.id.convList);
    unitType = (RadioGroup) findViewById(R.id.radioGroup);
    roundBox = (CheckBox) findViewById(R.id.chkRounded);
    formBox = (CheckBox) findViewById(R.id.chkFormula);
    imgView = (ImageView) findViewById(R.id.img);
    unitType.setOnCheckedChangeListener(
@Override
protected void onStart() {
    super.onStart();
    startDialog = new AlertDialog.Builder(MainActivity.this).create();
    startDialog.setTitle("Application started");
    startDialog.setMessage("This app can use to convert any units");
    startDialog.setButton(AlertDialog.BUTTON_NEUTRAL, "OK",
            new DialogInterface.OnClickListener() {
                public void onClick(DialogInterface dialog, int which) {
                    dialog.dismiss();
                }
            });
    startDialog.show();
Selanjutnya mengcopy paste  file java testB1basicactivity051 ke folder org.aplas.basicappx untuk dijalankan projeknya.
6.	Kemudian mendefinisikan resource string-array dan membuat fungsi radiogrup. Pertama membuka file string berformat xml yang terdapat dibawah folder res/values. Kemudian menambahkan jumlah pada semua string array serta mengcopy paste file gambar distance dan jarak ke folder drawable setelah itu membuka kelas main activity  dan membuat  event Ketika tipe unit radiogruo didalam fungsi onCreate:
@Override
public void onCheckedChanged(RadioGroup group, int checkedId) {
    RadioButton selected = (RadioButton) findViewById(checkedId);
    ArrayAdapter<CharSequence> adapter;
    inputTxt.setText("0");
    outputTxt.setText("0");
    if (selected.getText().equals("Temperature")) {
        adapter = ArrayAdapter.createFromResource(unitType.getContext(), R.array.tempList, android.R.layout.simple_spinner_item);
        imgView.setImageResource(R.drawable.temperature);
        imgView.setTag(R.drawable.temperature);
        adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
        unitOri.setAdapter(adapter);
        unitConv.setAdapter(adapter);
    } else if (selected.getText().equals("Distance")) {
        adapter = ArrayAdapter.createFromResource(unitType.getContext(), R.array.distList, android.R.layout.simple_spinner_item);
        imgView.setImageResource(R.drawable.distance);
        imgView.setTag(R.drawable.distance);
        adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
        unitOri.setAdapter(adapter);
        unitConv.setAdapter(adapter);
    }else {
        adapter = ArrayAdapter.createFromResource(unitType.getContext(), R.array.weightList, android.R.layout.simple_spinner_item);
        imgView.setImageResource(R.drawable.weight);
        imgView.setTag(R.drawable.weight);
        adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
        unitOri.setAdapter(adapter);
        unitConv.setAdapter(adapter);
    }
Selanjutnya mengcopy paste  file java elementTest dan ResoucerTest sert TestB1basicactivity061 ke folder org.aplas.basicappx untuk dijalankan projeknya.
7.	Pada tahap ini membuat dan menguji coba fungsi untuk melakukan konversi pada layout .pertama membuat fungsi void dengan nama doconvert dan membuat algoritma untuk mengkonversi jumlag dari input dan menghasilkan ke output
public void doConvert() {
    RadioButton selected = (RadioButton) findViewById(unitType.getCheckedRadioButtonId());
    double val = Double.parseDouble(inputTxt.getText().toString());
    double res = convertUnit(selected.getText().toString(), unitOri.getSelectedItem().toString(), unitConv.getSelectedItem().toString(), val);
    outputTxt.setText(strResult(res, roundBox.isChecked()));
Kemudian mengcopy paste  file java TestB1basicactivity071 ke folder org.aplas.basicappx untuk dijalankan projeknya.
8.	Mencoba dan menguji coba sebuah fungsi untuk menangkap aksi element pada file java main activity menambahkan event listener untuk menangkap event Ketika convertbutton diklik dan menambahkan event listener untuk menangkap event oralist, convlist dan roundbox berubah
convertBtn.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        doConvert();
    }
});
unitOri.setOnItemSelectedListener(new AdapterView.OnItemSelectedListener() {
    @Override
    public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {
        doConvert();
    }
    @Override
    public void onNothingSelected(AdapterView<?> parent) {
        return;
    }
});
unitConv.setOnItemSelectedListener(new AdapterView.OnItemSelectedListener() {
    @Override
    public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {
        doConvert();
    }
    @Override
    public void onNothingSelected(AdapterView<?> parent) {
        return;
    }
});
roundBox.setOnCheckedChangeListener(new CompoundButton.OnCheckedChangeListener() {
    @Override
    public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {
        doConvert();
    }
});
Kemudian mengcopy paste  file java TestB1basicactivity081 ke folder org.aplas.basicappx untuk dijalankan projeknya.
9.	Mencoba dan menguji coba untuk mengupload gambar formula dan membuat event listener Ketika checkbox formula sedang pengecekan. Pertama copy file gambar formula ke folder drawable kemudian membuka file activity_main berformat xml kemudaian membuat event listener untuk menangkap event Ketika roundbox berubah dan membuat  fungsi action untuk mengatur visibilitas "imgFormula" tergantung pada periksa kondisi "formBox". Jika "formBox" diperiksa maka "imgFormula" menjadi terlihat, jika tidak menjadi tidak terlihat.
roundBox.setOnCheckedChangeListener(new CompoundButton.OnCheckedChangeListener() {
    @Override
    public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {
        doConvert();
    }
});
formBox.setOnCheckedChangeListener(new CompoundButton.OnCheckedChangeListener() {
    @Override
    public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {
        ((ImageView)findViewById(R.id.imgFormula)).setVisibility((isChecked)?View.VISIBLE:View.INVISIBLE);
    }
});
Kemudian mengcopy paste  file java TestB1basicactivity091 dan TestB1basicactivity092 ke folder org.aplas.basicappx untuk dijalankan projeknya.

