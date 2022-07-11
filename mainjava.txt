
package com.example.gpa_calculater;

        import androidx.appcompat.app.AppCompatActivity;

        import android.annotation.SuppressLint;
        import android.os.Bundle;
        import android.view.View;
        import android.widget.Button;
        import android.widget.EditText;
        import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText et11,et12,et21,et22,et31,et32,et41,et42,et51,et52,et61,et62,et71,et72,et81,et82,et91,et92,et101,et102;
    Button btn;
    TextView result;


    @SuppressLint("SetTextI18n")
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        et11 = (EditText)findViewById(R.id.editText11);
        et21 = (EditText)findViewById(R.id.editText21);
        et31 = (EditText)findViewById(R.id.editText31);
        et41 = (EditText)findViewById(R.id.editText41);
        et51 = (EditText)findViewById(R.id.editText51);
        et61 = (EditText)findViewById(R.id.editText61);
        et71 = (EditText)findViewById(R.id.editText71);
        et81 = (EditText)findViewById(R.id.editText81);
        et91 = (EditText)findViewById(R.id.editText91);
        et101 = (EditText)findViewById(R.id.editText101);

        et12 = (EditText)findViewById(R.id.editText12);
        et22 = (EditText)findViewById(R.id.editText22);
        et32 = (EditText)findViewById(R.id.editText32);
        et42 = (EditText)findViewById(R.id.editText42);
        et52 = (EditText)findViewById(R.id.editText52);
        et62 = (EditText)findViewById(R.id.editText62);
        et72 = (EditText)findViewById(R.id.editText72);
        et82 = (EditText)findViewById(R.id.editText82);
        et92 = (EditText)findViewById(R.id.editText92);
        et102 = (EditText)findViewById(R.id.editText102);

        btn = (Button)findViewById(R.id.btn);
        result = (TextView)findViewById(R.id.result);


        btn.setOnClickListener((v) -> {

            int s1 = Integer.parseInt(et11.getText().toString());
            int s2 = Integer.parseInt(et21.getText().toString());
            int s3 = Integer.parseInt(et31.getText().toString());
            int s4 = Integer.parseInt(et41.getText().toString());
            int s5 = Integer.parseInt(et51.getText().toString());
            int s6 = Integer.parseInt(et61.getText().toString());
            int s7 = Integer.parseInt(et71.getText().toString());
            int s8 = Integer.parseInt(et81.getText().toString());
            int s9 = Integer.parseInt(et91.getText().toString());
            int s10 = Integer.parseInt(et101.getText().toString());

            float c1 = Float.parseFloat(et12.getText().toString());
            float c2 = Float.parseFloat(et22.getText().toString());
            float c3 = Float.parseFloat(et32.getText().toString());
            float c4 = Float.parseFloat(et42.getText().toString());
            float c5 = Float.parseFloat(et52.getText().toString());
            float c6 = Float.parseFloat(et62.getText().toString());
            float c7 = Float.parseFloat(et72.getText().toString());
            float c8 = Float.parseFloat(et82.getText().toString());
            float c9 = Float.parseFloat(et92.getText().toString());
            float c10 = Float.parseFloat(et102.getText().toString());

            float tc = c1+c2+c3+c4+c5+c6+c7+c8+c9+c10;

            float ans = ( (s1*c1) + (s2*c2) + (s3*c3) + (s4*c4) + (s5*c5) + (s6*c6) + (s7*c7) + (s8*c8) + (s9*c9) + (s10*c10) ) / tc;

            result.setText("GPA : " + ans);

        });
    }


}