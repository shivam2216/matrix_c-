// This code is used for applying operation on matrices.
//First:
//      Give number of rows and columns as r and s.
//      Enter the elemnts and enjoy the operations





#include<iostream>

using namespace std;

class matrix{

	private:

		int arr[20][20];

		int trans[20][20];

		int row;

		int col;

		public:

			matrix();

		void output();	

		void sum(matrix M);

		void sub(matrix M);

		void multiply(matrix M);

		void transpose();

		void tdis();

	};

	matrix :: matrix () {

			int r,c;

			cout<<"enter r and c: "<<endl;

			cin>>r>>c;

			row=r;

			col=c;

			cout<<"enter elements of the matrix: "<<endl;

				for ( int i=0; i<row; i++) {

		for (int j=0; j<col; j++) {

			cin>>arr[i][j];

			} } }

			

	void matrix :: output () {

				for ( int i=0; i<row; i++) {

		for (int j=0; j<col; j++) {

			cout<<arr[i][j]<<" "; } 

			cout<<endl;} }

	

		

		void matrix ::  sum(matrix M) {

			if( row==M.row&&col==M.col){

                 cout<<"addition of 2 matrix happens: "<<endl;

				for ( int i=0; i<row; i++) {

		for (int j=0; j<col; j++) {

			arr[i][j]= arr[i][j] + M.arr[i][j];

			cout<<arr[i][j]<<" ";

		}

		cout<<endl; 

        } 

        }

		else 

		cout<<"matrix cant be added."<<endl; }

		

			void matrix ::  sub(matrix M) {

				if ( row==M.row&&col==M.col) 

			{

			cout<<"subtraction  of 2 matrix happens: "<<endl;

				for ( int i=0; i<row; i++) {

		for (int j=0; j<col; j++) {

			arr[i][j]= arr[i][j] - M.arr[i][j];

			cout<<arr[i][j]<<" ";

		} 

		cout<<endl;} } 

		else 

		cout<<"matrix cant be subtracted."<<endl; } 

		

		

		void matrix  ::   multiply( matrix M) {

			if (row==M.col) { 

			cout<<"multiplication of the matrix are"<<endl;

			int pro[20][20];

			for ( int i=0; i<row; i++) {

				for ( int j=0;j<M.col; j++) {

					pro[i][j]=0;

					for ( int k=0; k<col; k++)

					pro[i][j]+= arr[i][k]*M.arr[k][j];

					cout<<pro[i][j]<<" ";

				} cout<<endl;

				}

			}

			else

			cout<<"matrix can not be multiplied"<<endl;

			}

		

		void matrix :: transpose () {

			for ( int i=0; i<row; i++) {

		for (int j=0; j<col; j++) {

			trans[j][i]=arr[i][j];

			

		}  } }

		 

		void matrix :: tdis () {

				for ( int i=0; i<col; i++) {

		for (int j=0; j<row; j++) {

			cout<<trans[i][j] << " ";

		} cout<<endl; } }

		

		

		

		

	int main ()	{

		matrix O1,O2;

		cout<<"the matrix 1 is: "<<endl;

		O1.output();

		cout<<"the matrix 2 is: "<<endl;

		O2.output();

		O1.sum(O2);

		O1.sub(O2);

		O1.multiply(O2);

		cout<<" transpose of the matrix is: "<<endl;

		O1.transpose();

	    O1.tdis();

		return 0;

	}
