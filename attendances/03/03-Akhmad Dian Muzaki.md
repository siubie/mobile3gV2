# Rangkuman Materi Activities and Intents dan JAVA DataBinding

Minggu Ke-03 Mata Kuliah Mobile
--

            Nama           : Akhmad Dian Muzaki
            NIM            : 1941720205
            No.Absen       : 03
            Dosen Pengampu : Putra Prima Arhandi, S.T., M.Kom.

Contents
--

- Activities -> komponen salah satu aplikasi yang berfungsi untuk interaksi pengguna ke sistem.

- Intents -> suatu object yang digunakan untuk mengeksekusi apa yang akan dilakukan oleh pengguna melalui sistem Android.

- Sending and Receiving Data -> Terdapat dua cara pengiriman yaitu, dengan URL dan key-value.

Dalam aktivitas (pengiriman) pertama:

1. Buat objek Intent
2. Masukkan data atau ekstra ke dalam maksud itu
3. Mulai aktivitas baru dengan startActivity()

Dalam aktivitas (penerimaan) kedua:

1. Dapatkan objek maksud saat aktivitas dimulai
2. Ambil data atau ekstra dari objek Intent.

- Navigation -> Adalah suatu komponen yang bisa memudahkan pengguna dalam menggunakan aplikasi.

Android MVVM DataBinding Java
--

DataBinding adalah pintu gerbang MVVM, yang mana ketika penggunaan databindingnya benar maka secara otomatis sudah tidak ada lagi findViewByld proses inflate layout jauh lebih cepat, aplikasi pun bisa lebih responsive dan binding di xml bisa di hubungkan dengan ViewModel dan LiveData.

Berikut adalah langkah-langkah yang harus dilakukan untuk membuat databinding pada project android:

1. Update Gradle
2. Update Layout XML di Activity/Fragment ke DataBinding Layout
3. Update Layout XML dengan Layout Expression
4. Ganti Inflate di Fragment/Activity
5. User Event (Handle Event dari XML)
6. Observe value dari ViewModel
7. Binding Adapter

Membuat konversi celcius ke suhu lain menggunakan method

# Membuat file Temperature.java

package org.aplas.basicappx;

class Temperature {
    private double celcius;

    Temperature() {
        this.celcius = 0;
    }

    double getCelcius() {
        return celcius;
    }

    void setCelcius(double celcius) {
        this.celcius = celcius;
    }

    double getFahrenheit() {
        return celcius * 1.8000 + 32.00;
    }

    void setFahrenheit(double fahrenheit) {
        this.celcius = (fahrenheit - 32) * 5 / 9;
    }

    double getKelvins() {
        return celcius + 273.15;
    }

    void setKelvins(double K) {
        this.celcius = K - 273.15;
    }

    double convert(String oriUnit, String convUnit, double value) {
        if (oriUnit.equals("°C") && convUnit.equals("°F")) {
            setCelcius(value);
            return getFahrenheit();
        } else if (oriUnit.equals("°C") && convUnit.equals("K")) {
            setCelcius(value);
            return getKelvins();
        } else if (oriUnit.equals("°F") && convUnit.equals("°C")) {
            setFahrenheit(value);
            return getCelcius();
        } else if (oriUnit.equals("°F") && convUnit.equals("K")) {
            setFahrenheit(value);
            return getKelvins();
        } else if (oriUnit.equals("K") && convUnit.equals("°C")) {
            setKelvins(value);
            return getCelcius();
        } else if (oriUnit.equals("K") && convUnit.equals("°F")) {
            setKelvins(value);
            return getFahrenheit();
        } else {
            return value;
        }
    }
}

# Membuat file Distance.java

package org.aplas.basicappx;

public class Distance {
    private double meter;

    public Distance() {
        this.meter = 0;
    }

    public double getMeter() {
        return meter;
    }

    public void setMeter(double meter) {
        this.meter = meter;
    }

    public double getInch() {
        return meter * 39.3701;
    }

    public void setInch(double inch) {
        this.meter = inch / 39.3701;
    }

    public double getMile() {
        return meter * 0.000621371;
    }

    public void setMile(double mile) {
        this.meter = mile / 0.000621371;
    }

    public double getFoot() {
        return meter * 3.28084;
    }

    public void setFoot(double feet) {
        this.meter = feet / 3.28084;
    }

    double convert(String oriUnit, String convUnit, double value) {
        if (oriUnit.equals("Mtr") && convUnit.equals("Inc")) {
            setMeter(value);
            return getInch();
        } else if (oriUnit.equals("Mtr") && convUnit.equals("Mil")) {
            setMeter(value);
            return getMile();
        } else if (oriUnit.equals("Mtr") && convUnit.equals("Ft")) {
            setMeter(value);
            return getFoot();
        } else if (oriUnit.equals("Inc") && convUnit.equals("Mtr")) {
            setInch(value);
            return getMeter();
        } else if (oriUnit.equals("Inc") && convUnit.equals("Mil")) {
            setInch(value);
            return getMile();
        } else if (oriUnit.equals("Inc") && convUnit.equals("Ft")) {
            setInch(value);
            return getFoot();
        } else if (oriUnit.equals("Mil") && convUnit.equals("Inc")) {
            setMile(value);
            return getInch();
        } else if (oriUnit.equals("Mil") && convUnit.equals("Mtr")) {
            setMile(value);
            return getMeter();
        } else if (oriUnit.equals("Mil") && convUnit.equals("Ft")) {
            setMile(value);
            return getFoot();
        } else if (oriUnit.equals("Ft") && convUnit.equals("Mtr")) {
            setFoot(value);
            return getMeter();
        } else if (oriUnit.equals("Ft") && convUnit.equals("Inc")) {
            setFoot(value);
            return getInch();
        } else if (oriUnit.equals("Ft") && convUnit.equals("Mil")) {
            setFoot(value);
            return getMile();
        } else {
            return value;
        }
    }
}

# Membuat file Weight.java
package org.aplas.basicappx;

public class Weight {
    private double gram;

    public Weight() {
        this.gram = 0;
    }

    public void setGram(double gram) {
        this.gram = gram;
    }

    public void setOunce(double ounce) {
        this.gram = ounce * 28.3495231;
    }

    public void setPound(double pound) {
        this.gram = pound * 453.59237;
    }

    public double getGram() {
        return this.gram;
    }

    public double getOunce() {
        return this.gram / 28.35;
    }

    public double getPound() {
        return this.gram / 454;
    }

    public double convert(String oriUnit, String convUnit, double value) {
        if (oriUnit.equals("Grm")) {
            this.setGram(value);
        } else if (oriUnit.equals("Onc")) {
            this.setOunce(value);
        } else if (oriUnit.equals("Pnd")) {
            this.setPound(value);
        }

        if (convUnit.equals("Grm"))
            value = this.getGram();
        else if (convUnit.equals("Onc"))
            value = this.getOunce();
        else if (convUnit.equals("Pnd"))
            value = this.getPound();

        return value;
    }
}

# Isi file MainActivity.java
package org.aplas.basicappx;

import android.content.DialogInterface;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.Button;
import android.widget.CheckBox;
import android.widget.CompoundButton;
import android.widget.EditText;
import android.widget.ImageView;
import android.widget.RadioButton;
import android.widget.RadioGroup;
import android.widget.Spinner;

import androidx.appcompat.app.AlertDialog;
import androidx.appcompat.app.AppCompatActivity;

import java.text.DecimalFormat;

public class MainActivity extends AppCompatActivity {

    String typeStr;
    double valuee;
    private AlertDialog startDialog;
    private Distance dist = new Distance();
    private Weight weight = new Weight();
    private Temperature temp = new Temperature();
    private Button convertBtn;
    private EditText inputTxt, outputTxt;
    private Spinner unitOri, unitConv;
    private RadioGroup unitType;
    private CheckBox roundBox, formBox;
    private ImageView imgView, imgFormula;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        convertBtn = findViewById(R.id.convertButton);
        inputTxt = findViewById(R.id.inputText);
        outputTxt = findViewById(R.id.outputText);
        unitOri = findViewById(R.id.oriList);
        unitConv = findViewById(R.id.convList);
        unitType = findViewById(R.id.radioGroup);
        roundBox = findViewById(R.id.chkRounded);
        formBox = findViewById(R.id.chkFormula);
        imgView = findViewById(R.id.img);
        imgFormula = findViewById(R.id.imgFormula);


        unitType.setOnCheckedChangeListener(
                new RadioGroup.OnCheckedChangeListener() {
                    @Override
                    public void onCheckedChanged(RadioGroup group, int checkedId) {
                        RadioButton selectedRB = findViewById(checkedId);
                        typeStr = selectedRB.getText().toString();
                        switch (typeStr) {
                            case "Temperature":
                                ArrayAdapter<CharSequence> adpTemp = ArrayAdapter.createFromResource(unitType.getContext(),
                                        R.array.tempList, android.R.layout.simple_spinner_item);
                                imgView.setImageResource(R.drawable.temperature);
                                adpTemp.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
                                unitOri.setAdapter(adpTemp);
                                unitConv.setAdapter(adpTemp);
                                inputTxt.setText("0");
                                outputTxt.setText("0");
                                break;
                            case "Distance":
                                ArrayAdapter<CharSequence> adpDist = ArrayAdapter.createFromResource(unitType.getContext(),
                                        R.array.distList, android.R.layout.simple_spinner_item);
                                imgView.setImageResource(R.drawable.distance);
                                adpDist.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
                                unitOri.setAdapter(adpDist);
                                unitConv.setAdapter(adpDist);
                                inputTxt.setText("0");
                                outputTxt.setText("0");
                                break;
                            case "Weight":
                                ArrayAdapter<CharSequence> adpWeight = ArrayAdapter.createFromResource(unitType.getContext(),
                                        R.array.weightList, android.R.layout.simple_spinner_item);
                                imgView.setImageResource(R.drawable.weight);
                                adpWeight.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
                                unitOri.setAdapter(adpWeight);
                                unitConv.setAdapter(adpWeight);
                                inputTxt.setText("0");
                                outputTxt.setText("0");
                                break;
                        }
                    }
                });

        convertBtn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                doConvert();
            }
        });

        unitOri.setOnItemSelectedListener(
                new AdapterView.OnItemSelectedListener() {
                    @Override
                    public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {
                        doConvert();
                    }

                    @Override
                    public void onNothingSelected(AdapterView<?> parent) {
                    }
                });

        unitConv.setOnItemSelectedListener(
                new AdapterView.OnItemSelectedListener() {
                    @Override
                    public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {
                        doConvert();
                    }

                    @Override
                    public void onNothingSelected(AdapterView<?> parent) {
                    }
                }
        );

        roundBox.setOnCheckedChangeListener(
                new CompoundButton.OnCheckedChangeListener() {
                    @Override
                    public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {
                        doConvert();
                    }
                }
        );

        formBox.setOnCheckedChangeListener(
                new CompoundButton.OnCheckedChangeListener() {
                    @Override
                    public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {
                        if (isChecked) {
                            imgFormula.setVisibility(View.VISIBLE);
                        } else {
                            imgFormula.setVisibility(View.INVISIBLE);
                        }
                    }
                }
        );
    }

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
    }

    protected double convertUnit(String unit, String ori, String conv, double value) {
        if (unit.equals("Temperature") && ori.equals("°F") && conv.equals("K")) {
            temp.setFahrenheit(value);
            return temp.getKelvins();
        } else if (unit.equals("Temperature") && ori.equals("K") && conv.equals("°C")) {
            temp.setKelvins(value);
            return temp.getCelcius();
        } else if (unit.equals("Distance") && ori.equals("Mtr") && conv.equals("Mil")) {
            dist.setMeter(value);
            return dist.getMile();
        } else if (unit.equals("Distance") && ori.equals("Mil") && conv.equals("Ft")) {
            dist.setMile(value);
            return dist.getFoot();
        } else if (unit.equals("Distance") && ori.equals("Inc") && conv.equals("Mtr")) {
            dist.setInch(value);
            return dist.getMeter();
        } else if (unit.equals("Weight") && ori.equals("Grm") && conv.equals("Pnd")) {
            weight.setGram(value);
            return weight.getPound();
        } else if (unit.equals("Weight") && ori.equals("Pnd") && conv.equals("Onc")) {
            weight.setPound(value);
            return weight.getOunce();
        }
        return value;
    }

    protected String strResult(double val, boolean rounded) {
        if (rounded) {
            DecimalFormat df = new DecimalFormat("#.##");
            return df.format(val);
        } else {
            DecimalFormat dff = new DecimalFormat("#.#####");
            return dff.format(val);
        }
    }

    void doConvert() {
        RadioButton selectedRB = findViewById(unitType.getCheckedRadioButtonId());
        typeStr = selectedRB.getText().toString();
        String ori = unitOri.getSelectedItem().toString();
        String conv = unitConv.getSelectedItem().toString();
        double input = Double.parseDouble(inputTxt.getText().toString());
        valuee = convertUnit(typeStr, ori, conv, input);
        outputTxt.setText(strResult(valuee, roundBox.isChecked()));
    }
}
