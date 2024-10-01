#!/bin/bash
flag=0
while [ $flag == 0 ]
do

read -p "Please insert your number: " x

rm -f "temp.file"
echo "$x" > "temp.file"
sed -i "s/[0-9]*//g" temp.file
a=$(<temp.file)

rm -f "temp.file"
echo "$x" > "temp.file"
sed -i "s/[I]*//g" temp.file
sed -i "s/[V]*//g" temp.file
sed -i "s/[X]*//g" temp.file
sed -i "s/[L]*//g" temp.file
sed -i "s/[C]*//g" temp.file
sed -i "s/[D]*//g" temp.file
sed -i "s/[M]*//g" temp.file
c=$(<temp.file)

flag=0

if [ "$a" == "" && $x <= 4000 ]; then
flag=1
fi

if [ "$c" == "" ]; then
flag=2
fi

done

rm -f "temp.file"

#Part 2: Transforming Number to Romanian Number
if [ $flag == 1 ]; then
echo -n "Your number is: "
while [ $x -ge 1000 ]
do
        echo -n M
        x=$(( $x - 1000 ))
done

s=0
while [ $x -ge 100 ]
do
        s=$(( $s + 1 ))
        x=$(( $x - 100 ))
done

case $s in
        1)
        echo -n C
        ;;
        2)
        echo -n CC
        ;;
        3)
        echo -n CCC
        ;;
        4)
        echo -n CD
        ;;
        5)
        echo -n D
        ;;
        6)
        echo -n DC
        ;;
        7)
        echo -n DCC
        ;;
        8)
        echo -n DCCC
        ;;
        9)
        echo -n CM
        ;;
esac

s=0
while [ $x -ge 10 ]
do
        s=$(( $s + 1 ))
        x=$(( $x - 10 ))
done

case $s in
        1)
        echo -n X
        ;;
        2)
        echo -n XX
        ;;
        3)
        echo -n XXX
        ;;
        4)
        echo -n XL
        ;;
        5)
        echo -n L
        ;;
        6)
        echo -n LX
        ;;
        7)
        echo -n LXX
        ;;
        8)
        echo -n LXXX
        ;;
        9)
        echo -n XC
        ;;
esac

case $x in
        1)
        echo -n I
        ;;
        2)
        echo -n II
        ;;
        3)
        echo -n III
        ;;
        4)
        echo -n IV
        ;;
        5)
        echo -n V
        ;;
        6)
        echo -n VI
        ;;
        7)
        echo -n VII
        ;;
        8)
        echo -n VIII
        ;;
        9)
        echo -n IX
        ;;
esac

fi

#Part 3: Transforming Romanian Numember into Number
if [ $flag == 2 ]; then

ar=0
em=`expr length $x`
th="${x: -1}"

if [ "$th" == "I" ]; then
	ar=$(( $ar + 1 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "I" ]; then
	ar=$(( $ar + 1 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "I" ]; then
	ar=$(( $ar + 1 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "V" ]; then
	ar=$(( $ar + 5 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "I" ]; then
	ar=$(( $ar - 1 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "X" ]; then
	ar=$(( $ar + 10 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "I" ]; then
	ar=$(( $ar - 1 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "X" ]; then
	ar=$(( $ar + 10 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "X" ]; then
	ar=$(( $ar + 10 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "X" ]; then
	ar=$(( $ar + 10 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "L" ]; then
	ar=$(( $ar + 50 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "X" ]; then
	ar=$(( $ar - 10 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "C" ]; then
	ar=$(( $ar + 100 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "X" ]; then
	ar=$(( $ar - 10 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "C" ]; then
	ar=$(( $ar + 100 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "C" ]; then
	ar=$(( $ar + 100 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "C" ]; then
	ar=$(( $ar + 100 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "D" ]; then
	ar=$(( $ar + 500 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "C" ]; then
	ar=$(( $ar - 100 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "M" ]; then
	ar=$(( $ar + 1000 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "C" ]; then
	ar=$(( $ar - 100 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "M" ]; then
	ar=$(( $ar + 1000 ))
	em=$(( em - 1 ))
	x=`expr substr $x 1 $em`
	th="${x: -1}"
fi

if [ "$th" == "M" ]; then
        ar=$(( $ar + 1000 ))
        em=$(( em - 1 ))
        x=`expr substr $x 1 $em`
        th="${x: -1}"
fi

if [ "$th" == "M" ]; then
        ar=$(( $ar + 1000 ))
        em=$(( em - 1 ))
        x=`expr substr $x 1 $em`
        th="${x: -1}"
fi


echo -n "Your number is: " $ar
fi

echo ""
