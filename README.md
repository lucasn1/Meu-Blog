## Bem vindo!!

Página criada para o repositório de trabalhos , códigos e relatórios da faculdade.

### Código de diferenciação Numérica em C .

código referente ao trabalho de diferenciação Numérica contendo 3 fórmulas :
- Progressiva (avançada)
- Regressiva 
- Central

Avaliação : 
1- Para um funcionamento ,e entendimento, melhor deveria ser usado case e não a estrutura de decisão usada.
2- Número exagerado de variáveis 
3- Adotar funções deixaria o código mais limpo

código está funcionando



```markdown
# include <stdio.h>
# include <conio.h>
# include <math.h>
# include <stdlib.h>

void main ()
{
    int opcao;
    printf ("Entre com a opcao desejada:\n");
    printf ("1- Diferenca progressiva (ou avancada)\n");
    printf ("2- Diferenca regressiva (ou recuada)\n");
    printf ("3- Diferenca central\n");
    scanf ("%d", &opcao);
        if (opcao == 1)
            {
                int opcao2;
                printf ("\nQual a funcao desejada?\n");
                printf ("1- cos(x)\n");
                printf ("2- e^-x\n");
                printf ("3- e^-x^2\n");
                scanf ("%d", &opcao2);
                    if (opcao2 == 1)
                        {
                           	float x, h, h1, h2, f, f1, f2, cosseno = 0, cosseno2 = 0, cosseno3 = 0, cosseno4 = 0; 
                            printf ("\nEntre com o ponto:");
                            scanf ("%f", &x);
                            printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                            scanf ("%f %f %f", &h, &h1, &h2);
                            cosseno = cos(x);
                            cosseno2 = cos(x + h);
                            cosseno3 = cos(x + h1);
                            cosseno4 = cos(x + h2);
                            f = (cosseno2 - cosseno)/(h);
                            f1 = (cosseno3 - cosseno)/(h1);
                            f2 = (cosseno4 - cosseno)/(h2);
                            printf ("\nA derivada e:%.6f\n", f);
                            printf ("A derivada e:%.6f\n", f1);
                            printf ("A derivada e:%.5f\n", f2);
                        }

                    else if (opcao2 == 2)
                        {
                            float x, h, h1, h2, f, f1, f2, k, t, t1, t2, l, l1, l2, e = 0;
                            printf ("\nEntre com o ponto:");
                            scanf ("%f", &x);
                            printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                            scanf ("%f %f %f", &h, &h1, &h2);
                            e = 2.71828182846;
                            k = pow (e, -x);
                            l = - (x + h);
                            l1 = - (x + h1);
                            l2 = - (x + h2);
                            t = pow (e, l);
                            t1 = pow (e, l1);
                            t2 = pow (e, l2);
                            f = (t-k)/h;
                            f1 = (t1-k)/h1;
                            f2 = (t2-k)/h2;
                            printf ("\nA derivada e:%.6f\n", f);
                            printf ("A derivada e:%.6f\n", f1);
                            printf ("A derivada e:%.6f\n", f2);
                        }

                    else if (opcao2 == 3)
                        {
                            float x, h, h1, h2, f, f1, f2, k, e=0, t, t1, t2, b, c, c1, c2, d, d1, d2;
                            printf ("\nEntre com o ponto:");
                            scanf ("%f", &x);
                            printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                            scanf ("%f %f %f", &h, &h1, &h2);
                            e =  2.7182818;
                            b = pow (x, 2);
                            k = pow (e, -b);
                            c = (x + h);
                            c1 = (x + h1);
                            c2 = (x + h2);
                            d = pow (c, 2);
                            d1 = pow (c1, 2);
                            d2 = pow (c2, 2);
                            t = pow (e, -d);
                            t1 = pow (e, -d1);
                            t2 = pow (e, -d2);
                            f = (t-k)/h;
                            f1 = (t1-k)/h1;
                            f2 = (t2-k)/h2;
                            printf ("\nA derivada e:%.5f\n", f);
                            printf ("A derivada e:%.5f\n", f1);
                            printf ("A derivada e:%.5f\n", f2);
                        }

                    else
                    {
                        printf ("\nOpcao invalida");
                    }
            }
        else if (opcao == 2)
            {
                int opcao3;
                printf ("\nQual a funcao desejada?\n");
                printf ("1- cos(x)\n");
                printf ("2- e^-x\n");
                printf ("3- e^-x^2\n");
                scanf ("%d", &opcao3);
                if (opcao3 == 1)
                    {
                        float x, h, h1, h2, f, f1, f2, cosseno = 0, cosseno2 = 0, cosseno3 = 0, cosseno4 = 0;
                        printf ("\nEntre com o ponto:");
                        scanf ("%f", &x);
                        printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                        scanf ("%f %f %f", &h, &h1, &h2);
                        cosseno = cos(x);
                        cosseno2 = cos(x - h);
                        cosseno3 = cos(x - h1);
                        cosseno4 = cos(x - h2);
                        f = (cosseno - cosseno2)/(h);
                        f1 = (cosseno - cosseno3)/(h1);
                        f2 = (cosseno - cosseno4)/(h2);
                        printf ("\nA derivada e:%.6f\n", f);
                        printf ("A derivada e:%.6f\n", f1);
                        printf ("A derivada e:%.6f\n", f2);
                    }

                else if (opcao3 == 2)
                    {
                        float x, h, h1, h2, f, f1, f2, k, t, t1, t2, l, l1, l2, e = 0;
                        printf ("\nEntre com o ponto:");
                        scanf ("%f", &x);
                        printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                        scanf ("%f %f %f", &h, &h1, &h2);
                        e = 2.71828182846;
                        k = pow (e, -x);
                        l = - (x - h);
                        l1 = - (x - h1);
                        l2 = - (x - h2);
                        t = pow (e, l);
                        t1 = pow (e, l1);
                        t2 = pow (e, l2);
                        f = (k-t)/h;
                        f1 = (k-t1)/h1;
                        f2 = (k-t2)/h2;
                        printf ("\nA derivada e:%.6f\n", f);
                        printf ("A derivada e:%.6f\n", f1);
                        printf ("A derivada e:%.5f\n", f2);
                    }

                else if (opcao3 == 3)
                    {
                        float x, h, h1, h2, f, f1, f2, k, e=0, t, t1, t2, b, c, c1, c2, d, d1, d2;
                        printf ("\nEntre com o ponto:");
                        scanf ("%f", &x);
                        printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                        scanf ("%f %f %f", &h, &h1, &h2);
                        e =  2.7182818;
                        b = pow (x, 2);
                        k = pow (e, -b);
                        c = (x - h);
                        c1 = (x - h1);
                        c2 = (x - h2);
                        d = pow (c, 2);
                        d1 = pow (c1, 2);
                        d2 = pow (c2, 2);
                        t = pow (e, -d);
                        t1 = pow (e, -d1);
                        t2 = pow (e, -d2);
                        f = (k-t)/h;
                        f1 = (k-t1)/h1;
                        f2 = (k-t2)/h2;
                        printf ("\nA derivada e:%.5f\n", f);
                        printf ("A derivada e:%.5f\n", f1);
                        printf ("A derivada e:%.5f\n", f2);
                    }

                else
                    {
                        printf ("\nOpcao invalida");
                    }
            }
         else if (opcao == 3)
            {
                int opcao4;
                printf ("\nQual a funcao desejada?\n");
                printf ("1- cos(x)\n");
                printf ("2- e^-x\n");
                printf ("3- e^-x^2\n");
                scanf ("%d", &opcao4);
                if (opcao4 == 1)
                    {
                        float x, h, h1, h2, f, f1, f2, cosseno = 0, cosseno2 = 0, cosseno3 = 0, cosseno4 = 0, cosseno5 = 0, cosseno6 = 0;
                        printf ("\nEntre com o ponto: ");
                        scanf ("%f", &x);
                        printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                        scanf ("%f %f %f", &h, &h1, &h2);
                        cosseno = cos(x + h);
                        cosseno2 = cos(x + h1);
                        cosseno3 = cos(x + h2);
                        cosseno4 = cos(x - h);
                        cosseno5 = cos(x - h1);
                        cosseno6 = cos(x - h2);
                        f = (cosseno - cosseno4)/(2*h);
                        f1 = (cosseno2 - cosseno5)/(2*h1);
                        f2 = (cosseno3 - cosseno6)/(2*h2);
                        printf ("\nA derivada e:%.6f\n", f);
                        printf ("A derivada e:%.6f\n", f1);
                        printf ("A derivada e:%.5f\n", f2);
                    }

                else if (opcao4 == 2)
                    {
                        float x, h, h1, h2, f, f1, f2, t, t1, t2, t3, t4, t5, l, l1, l2, l3, l4, l5, e;
                        printf ("\nEntre com o ponto:");
                        scanf ("%f", &x);
                        printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                        scanf ("%f %f %f", &h, &h1, &h2);
                        e =  2.7182818;
                        l = (x + h);
                        l1 = (x + h1);
                        l2 = (x + h2);
                        l3 = (x - h);
                        l4 = (x - h1);
                        l5 = (x - h2);
                        t = pow (e, -l);
                        t1 = pow (e, - l1);
                        t2 = pow (e, - l2);
                        t3 = pow (e, - l3);
                        t4 = pow (e, - l4);
                        t5 = pow (e, - l5);
                        f = (t - t3)/(2*h);
                        f1 = (t1 - t4)/(2*h1);
                        f2 = (t2 - t5)/(2*h2);
                        printf ("\nA derivada e:%.6f\n", f);
                        printf ("A derivada e:%.6f\n", f1);
                        printf ("A derivada e:%.6f\n", f2);
                    }

                else if (opcao4 == 3)
                    {
                        float x, h, h1, h2, f, f1, f2, e=0, t, t1, t2, t3, t4, t5, c, c1, c2, c3, c4, c5, l, l1, l2, l3, l4, l5;
                        printf ("\nEntre com o ponto:");
                        scanf ("%f", &x);
                        printf ("Entre com 3 valores para h (aperte enter a cada valor digitado):\n");
                        scanf ("%f %f %f", &h, &h1, &h2);
                        e =  2.7182818;
                        l = (x + h);
                        l1 = (x + h1);
                        l2 = (x + h2);
                        l3 = (x - h);
                        l4 = (x - h1);
                        l5 = (x - h2);
                        c = pow (l, 2);
                        c1 = pow (l1, 2);
                        c2 = pow (l2, 2);
                        c3 = pow (l3, 2);
                        c4 = pow (l4, 2);
                        c5 = pow (l5, 2);
                        t = pow (e, - c);
                        t1 = pow (e, - c1);
                        t2 = pow (e, - c2);
                        t3 = pow (e, - c3);
                        t4 = pow (e, - c4);
                        t5 = pow (e, - c5);
                        f = (t - t3)/(2*h);
                        f1 = (t1 - t4)/(2*h1);
                        f2 = (t2 - t5)/(2*h2);
                        printf ("\nA derivada e:%.6f\n", f);
                        printf ("A derivada e:%.6f\n", f1);
                        printf ("A derivada e:%.5f\n", f2);
                    }
                else
                    {
                        printf ("\nOpcao invalida");
                    }
            }

            else
            {
                printf ("\nOpcao invalida");
            }
}

```
### Tela de login e senha Python + Tkinter






```markdown

from tkinter import *


janela = Tk()

lb1 = Label(janela, text="Login: ")
lb2 = Label(janela, text="Senha: ")

ed1 = Entry(janela,)
ed2 = Entry(janela,)

bt1 = Button(janela, text="Confirmar")

lb1.grid(row=0, column=0)
lb2.grid(row=1, column=0)
ed1.grid(row=0, column=1)
ed2.grid(row=1, column=1)
bt1.grid(row=2, column=1)



janela.geometry("200x100+100+100")
janela.mainloop()
```


### Sobre mim

#Cursando Engenharia da computação  
#Uerj / Iprj
#20 anos


