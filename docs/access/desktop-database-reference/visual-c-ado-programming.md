---
title: Programación de ADO con Visual C++
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a890b4906fb9f207f12ff17ef0d3ccf1a97a44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302775"
---
# <a name="visual-c-ado-programming"></a>Programación de ADO con Visual C++

**Se aplica a:** Access 2013, Office 2013

La Referencia de la API de ADO describe la funcionalidad de la interfaz de programación de aplicaciones (API) de ADO mediante una sintaxis similar a Microsoft Visual Basic. Aunque la audiencia prevista es todos los usuarios, los programadores de ADO emplean diversos lenguajes, como Visual Basic, Visual C++ ** \#** (con y sin la Directiva Import) y Visual J++ (con el paquete de clases ADO/WFC).

Para dar cabida a esta diversidad, los [Índices de sintaxis de ADO para Visual C++](using-ado-with-microsoft-visual-c.md) proporcionan sintaxis específica de Visual C++ con vínculos a descripciones comunes de funcionalidad, parámetros, comportamientos excepcionales, etc., en la Referencia de la API.

ADO se implementa con interfaces COM (Modelo de objetos componentes). Sin embargo, es más fácil para los programadores trabajar con COM en algunos lenguajes de programación que en otros. Por ejemplo, casi todos los detalles del uso de COM se manejan implícitamente en Visual Basic, mientras que en Visual C++ son los programadores quienes deben manejar esos detalles.

En las secciones siguientes se resumen los detalles de los programadores de C y C++ ** \#** que usan ADO y la Directiva de importación. Se centra en los tipos de datos específicos de COM (**Variant**, **BSTR**y **SAFEARRAY**) y en el control\_de\_errores (error de com).

## <a name="using-the-import-compiler-directive"></a>Uso de \#la Directiva del compilador de importación

La Directiva del compilador de Visual C++ de ** \#importación** simplifica el trabajo con los métodos y propiedades de ADO. La directiva toma el nombre de un archivo que contiene una biblioteca de tipos, tal como la dll de ADO (Msado15.dll), y genera archivos de encabezado que contienen declaraciones typedef, punteros inteligentes para interface y constantes enumeradas. Cada interfaz se encapsula o engloba en una clase.

Para cada operación dentro de una clase (es decir una llamada a método o propiedad), existe una declaración para llamar a la operación directamente (es decir, la forma "original" de la operación) y una declaración para llamar a la operación original y generar un error COM si la operación no se ejecuta correctamente. Si la operación es una propiedad, suele existir una directiva del compilador que crea una sintaxis alternativa para la operación que tiene sintaxis similar a Visual Basic.

Las operaciones que recuperan el valor de una propiedad tienen nombres de la forma, **Get * * * Property*. Las operaciones que establecen el valor de una propiedad tienen los nombres de la propiedad form, **Put * * **. Las operaciones que establecen el valor de una propiedad con un puntero a un objeto ADO tienen nombres con el formato **PutRef * * * Property*.

Puede obtener o establecer una propiedad con llamadas de este tipo:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Uso de directivas de propiedad

La Directiva del compilador ** \_declspec (Property...) es una extensión de lenguaje C específica de Microsoft que declara que una función utilizada como propiedad tiene una sintaxis \_** alternativa. Como resultado, puede establecer u obtener valores de una propiedad de forma similar a Visual Basic. Por ejemplo, puede establecer y obtener una propiedad de este modo:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Tenga en cuenta que no tiene que escribir este código:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

El compilador generará la llamada de propiedad **Get * * *-*, **Put**-o **PutRef * * ** correspondiente en función de la sintaxis alternativa que se declara y de si la propiedad se está leyendo o escribiendo.

La Directiva del compilador ** \_ \_declspec (Property...)** solo puede declarar la sintaxis alternativa **Get**, **Put**o **Get** y **Put** para una función. Las operaciones de sólo lectura únicamente tienen una declaración **get**; las operaciones de sólo escritura únicamente tienen una declaración **put**; las operaciones de lectura y escritura tienen ambas declaraciones **get** y **put**.

Solo se pueden realizar dos declaraciones con esta Directiva; sin embargo, cada propiedad puede tener tres funciones de propiedad: **Get * * ** Property, **Put * * * Property*y **PutRef * * ** Property. En ese caso, sólo dos formas de la propiedad presentan sintaxis alternativa.

Por ejemplo, la propiedad **ActiveConnection** del objeto **Command** se declara con una sintaxis alternativa para **Get * * * ActiveConnection* y **PutRef * * * ActiveConnection*. La sintaxis de **PutRef** constituye una buena elección, ya que, en la práctica, deseará establecer un objeto **Connection** abierto (es decir, un puntero a un objeto**Connection**) en esta propiedad. Por otra parte, el objeto **Recordset** tiene operaciones de **Get**-, **Put**-y **PutRef * * ** , pero ninguna sintaxis alternativa.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Colecciones, el método GetItem y la propiedad Item

ADO define varias colecciones, incluidas **Fields**, **Parameters**, **Properties** y **Errors**. En Visual C++, el método **GetItem (***Índice***)** devuelve un miembro de la colección. *Índice* es de un tipo **Variant**, cuyo valor es el índice numérico del miembro de la colección o una cadena que contiene el nombre del miembro.

La **** **** ** \_ \_Directiva del compilador declspec (Property...)** declara la propiedad Item como una sintaxis alternativa para el método GetItem () fundamental de cada colección. La sintaxis alternativa utiliza corchetes y es similar a una referencia a matriz. En general, las dos formas son similares a lo siguiente:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Por ejemplo, asigne un valor a un campo de un objeto **Recordset**, denominado ***rs***, derivado de la tabla ** authors** de la base de datos **pubs**. Utilice la **propiedad Item ()** para tener acceso al **tercer campo** de la colección **Fields** del objeto **Recordset** (las colecciones se indizan desde cero; suponga que el tercer campo se denomina ***au\_fname***). A continuación, llame al método **Value()** sobre el objeto **Field** para asignar un valor de cadena.

Esto se puede expresar en Visual Basic de las siguientes cuatro maneras (las últimas dos formas son exclusivas de Visual Basic; otros lenguajes no tienen equivalentes):

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

El equivalente en Visual C++ a las dos primeras formas anteriores es:

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-o bien-(también se muestra la sintaxis alternativa de la propiedad **Value** )

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Tipos de datos específicos de COM

En general, cualquier tipo de datos de Visual Basic que se encuentra en la Referencia de la API de ADO tiene un equivalente en Visual C++. Éstos incluyen tipos de datos estándar, tales como **unsigned char** para un **Byte** de Visual Basic, **short** para **Integer** y **long** para **Long**. Busque en los Índices de la sintaxis para ver qué se requiere exactamente para los operandos de un método o una propiedad dados.

Las excepciones a esta regla son los tipo de datos específicos de COM: **Variant**, **BSTR** y **SafeArray**.

### <a name="variant"></a>Variant

Un **Variant** es un tipo de datos estructurados que contiene un miembro de valor y un miembro de tipo de datos. Un **Variant** puede contener una amplia variedad de otros tipos de datos, incluidos otro Variant, BSTR, Boolean, IDispatch, puntero a IUnknown, moneda, fecha, etc. COM también proporciona métodos que facilitan la conversión de un tipo de datos en otro.

La ** \_clase\_Variant t** encapsula y administra el tipo de datos **Variant** .

Cuando la referencia de la API de ADO indica que un operando de un método o una propiedad toma un valor, suele significar que el valor se pasa en una ** \_Variant\_t**.

Esta regla se cumple explícitamente cuando la sección **Parámetros** de los temas de la Referencia de la API de ADO indica que un operando es de tipo **Variant**. Una excepción es cuando la documentación indica explícitamente que el operandos toma un tipo de datos estándar, como **Long**, **Byte** o una enumeración. Otra excepción es cuando el operando toma un **String**.

### <a name="bstr"></a>BSTR

Un **BSTR** (**B**asic **STR**ing) es un tipo de datos estructurados que contiene una cadena de caracteres y la longitud de la cadena. COM proporciona métodos para asignar, manipular y liberar un **BSTR**.

La ** \_clase\_BSTR t** encapsula y administra el tipo de datos **BSTR** .

Cuando la referencia de la API de ADO indica que un método o una propiedad toma un valor de **cadena** , significa que el valor está en forma de ** \_BSTR\_t**.

#### <a name="casting-variantt-and-bstrt-classes"></a>Clases \_Variant\_t y \_BSTR\_t de conversión

A menudo, no es necesario codificar explícitamente un ** \_tipo Variant\_t** o ** \_BSTR\_t** en un argumento para una operación. Si la ** \_clase\_Variant t** o ** \_BSTR\_t** tiene un constructor que coincide con el tipo de datos del argumento, el compilador generará ** \_la\_Variant t** o ** \_ BSTR\_t**.

Sin embargo, si el argumento es ambiguo, es decir, el tipo de datos del argumento coincide con más de un constructor, deberá convertir el argumento explícitamente al tipo de datos apropiado para llamar al constructor correcto.

Por ejemplo, la declaración para el método **Recordset::Open** es:

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

El argumento ActiveConnection toma una referencia a ** \_\_Variant t**, que puede codificar como una cadena de conexión o un puntero a un objeto **Connection** abierto.

La ** \_variante\_t** correcta se construirá implícitamente si se pasa una cadena como "DSN = pubs; UID = SA; pwd =;" o un puntero como "(IDispatch \*) pConn".

O puede codificar explícitamente ** \_un\_valor Variant t** que contenga un\_puntero\_como "Variant t \*((IDispatch) pConn, true)". La conversión, (IDispatch \*), resuelve la ambigüedad con otro constructor que toma un puntero a una interfaz IUnknown.

Es un hecho crucial (aunque raramente mencionado) que ADO es una interfaz IDispatch. Siempre que un puntero a un objeto ADO se deba pasar como un **Variant**, es necesario convertir explícitamente ese puntero a un puntero a un interfaz IDispatch.

El último caso codifica explícitamente el segundo argumento booleano del constructor con su valor predeterminado opcional true. Este argumento hace que el constructor **Variant** llame a su método **AddRef**(), que compensa a ADO llamar automáticamente al ** \_método\_Variant t:: Release**() cuando finaliza la llamada al método o la propiedad de ADO.

### <a name="safearray"></a>Matriz

Un **SafeArray** es un tipo de datos estructurados que contiene una matriz de otros tipos de datos. Un **SafeArray** se denomina *safe* (seguro) debido a que contiene información sobre los límites de cada dimensión de la matriz y limita el acceso a los elementos de la matriz a esos límites.

Cuando la Referencia de la API de ADO indica que un método o una propiedad acepta o devuelve una matriz, significa que el método o la propiedad acepta o devuelve un **SafeArray** no una matriz nativa de C/C++.

Por ejemplo, el segundo parámetro del método **OpenSchema** del objeto **Conection** requiere una matriz de valores **Variant**. Esos valores **Variant** se deben pasar como elementos de un **SafeArray**, y ese **SafeArray** se debe establecer como el valor de otro **Variant**. Es ese otro **Variant** el que se pasa como el segundo argumento de **OpenSchema**.

Como ejemplos adicionales, el primer argumento del método **Find** es un **Variant** cuyo valor es un **SafeArray** unidimensional, cada uno de los argumentos primero y segundo opcionales de **AddNew** es un **SafeArray** unidimensional y el valor devuelto del método **GetRows** es un **Variant** cuyo valor es un **SafeArray** bidimensional.

## <a name="missing-and-default-parameters"></a>Parámetros predeterminados y ausentes

Visual Basic permite que falten parámetros en los métodos. Por ejemplo, el método **Open** de un objeto **Recordset** tiene cinco parámetros, pero se pueden omitir parámetros intermedios y no incluir parámetros finales. Se usará entonces un **BSTR** o **Variant** predeterminado según el tipo de datos del operando que falte.

En C/C++, se deben especificar todos los operandos. Si desea especificar un parámetro que falta cuyo tipo de datos es una cadena, especifique un ** \_BSTR\_t** que contenga una cadena nula. Si desea especificar un parámetro que falta cuyo tipo de datos es **Variant**, especifique un\_\_ ** \_valor Variant\_t** con un valor de DISP e PARAMNOTFOUND y un tipo de error\_VT. Como alternativa, especifique la constante ** \_t\_** equivalente de variante, **vtMissing**, que proporciona la Directiva de ** \#importación** .

Existen tres métodos que constituyen excepciones al uso típico de **vtMissing**. Éstos son los métodos **Execute** de los objetos **Connection** y **Command**, y el método **NextRecordset** del objeto **Recordset**. Las siguientes son sus firmas:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Los parámetros *RecordsAffected* y *Parameters*son punteros a un **Variant**. *Parameters* es un parámetro de entrada que especifica la dirección de un **Variant** que contiene un parámetro único, o una matriz de parámetros, que modificará el comando que se va a ejecutar. *RecordsAffected* es un parámetro de salida que especifica la dirección de un **Variant** donde se devuelve el número de filas afectadas por el método.

En el método **Execute** del objeto **Command** , indique que no se especifica ningún parámetro estableciendo *los parámetros* en \&vtMissing (que se recomienda) o en el puntero NULL (es decir, **null** o cero (0)). Si *Parameters* se establece en el puntero nulo, el método sustituye internamente el equivalente de **vtMissing** y, a continuación, completa la operación.

En todos los métodos, indique que no se debe devolver el número de registros afectados; puede hacerlo estableciendo *RecordsAffected* en un puntero nulo. En este caso, el puntero nulo no es tanto un parámetro que falta como una indicación de que el método debería descartar el número de registros afectados.

Por tanto, para estos tres métodos, es correcto codificar del siguiente modo:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Control de errores

In COM, most operations return an HRESULT return code that indicates whether a function completed successfully. La Directiva de ** \#importación** genera código de contenedor alrededor de cada método o propiedad "sin procesar" y comprueba el HRESULT devuelto. Si el HRESULT indica un error, el código de contenedor produce un error COM al \_llamar\_a\_errorex () con el código de retorno HRESULT como un argumento. COM error objects can be caught in a **try**-**catch** block. (Por motivos de eficacia, Capture una referencia a un ** \_objeto\_de error com** ).

Recuerde que éstos son errores de ADO (resultado de una operación ADO). Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.

La ** \#Directiva Import** sólo crea rutinas de tratamiento de errores para métodos y propiedades declarados en la. dll de ADO. Sin embargo, puede aprovechar este mismo mecanismo de tratamiento de errores escribiendo su propia función en línea o macro de comprobación de errores. Vea el tema [Extensiones de Visual C++](visual-c-extensions-for-ado.md) o el código de la sección siguiente para obtener ejemplos.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Equivalentes de Visual C++ de las convenciones de Visual Basic

A continuación, se muestra un resumen de diversas convenciones de la documentación de ADO, codificadas en Visual Basic, así como sus equivalentes en Visual C++.

### <a name="declaring-an-ado-object"></a>Declaración de un objeto de ADO

En Visual Basic, una variable de objeto ADO (en este caso, de un objeto **Recordset**) se declara del siguiente modo:

```vb 
 
Dim rst As ADODB.Recordset 
```

La cláusula "ADODB. Recordset "es el ProgID del objeto **Recordset** tal como se define en el registro. Una instancia nueva de un objeto **Record** se declara del siguiente modo:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-o

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

En Visual C++, la ** \#** Directiva de importación genera declaraciones de tipo de puntero inteligente para todos los objetos de ADO. Por ejemplo, una variable que apunta a un ** \_objeto Recordset** es del tipo ** \_RecordsetPtr**y se declara del siguiente modo:

```cpp 
 
_RecordsetPtr rs; 
```

Una variable que apunta a una nueva instancia de un ** \_objeto Recordset** se declara del siguiente modo:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-o

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-o

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

Después de llamar al método **CreateInstance**, la variable se puede utilizar de la manera siguiente:

```cpp 
 
rs->Open(...); 
```

Observe que, en un caso, el operador "." se utiliza como si la variable fuera una instancia de una clase (RS. CreateInstance) y, en otro caso, el operador "\>-" se utiliza como si la variable fuera un puntero a una interfaz (RS-\>Open).

Una variable se puede usar de dos maneras porque el operador "\>-" está sobrecargado para permitir que una instancia de una clase se comporte como un puntero a una interfaz. Un miembro de clase privada de la variable de instancia contiene un puntero a la interfaz del ** \_objeto Recordset** ; el operador "\>-" devuelve ese puntero; y el puntero devuelto tiene acceso a los miembros del objeto ** \_Recordset** .

### <a name="coding-a-missing-parameter"></a>Codificar un parámetro que falta

#### <a name="string"></a>String

Cuando necesite codificar en Visual Basic un operando **String** ausente, simplemente omita el operando. Deberá especificar el operando en Visual C++. Codifique un ** \_BSTR\_t** que tenga una cadena vacía como un valor.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

Cuando necesite codificar en Visual Basic un operando **Variant** ausente, simplemente omita el operando. En Visual C++, deberá especificar todos los operandos. Codifique un parámetro **Variant** ausente con ** \_Variant\_t** establecido en el valor especial, DISP\_e\_PARAMNOTFOUND y tipo, error VT\_. Como alternativa, especifique **vtMissing**, que es una constante predefinida equivalente especificada por la Directiva de ** \#importación** .

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-o use-

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Declaración de una variante

En Visual Basic, un tipo **Variant** se declara con la instrucción **Dim** del siguiente modo:

```vb 
 
Dim VariableName As Variant 
```

En Visual C++, declare una variable como ** \_tipo\_Variant t**. A continuación se muestran algunas declaraciones de ** \_Variant\_t** esquemáticas.

> [!NOTE]
> Estas declaraciones simplemente proporcionan una idea general de cómo podría codificar su propio programa. Para obtener más información, vea los ejemplos siguientes y la documentación de Visual C++.

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>Uso de matrices de variantes

En Visual Basic, las matrices de **Variants** se pueden codificar con la instrucción **Dim** o utilizar la función **Array**, tal como se muestra en el código de ejemplo siguiente:

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

El siguiente ejemplo de Visual C++ muestra el uso de un **SAFEARRAY** usado con una ** \_Variant\_t**.

> [!NOTE]
> Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.

1. Una vez más, se define la función inline TESTHR() para aprovechar el mecanismo de control de errores existente.

2. Sólo necesitará una matriz unidimensional, de forma que pueda utilizar **SafeArrayCreateVector** en lugar de la declaración de propósito general **SAFEARRAYBOUND** y la función **SafeArrayCreate**. El código que utiliza **SafeArrayCreate** tiene el siguiente aspecto:
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. El esquema identificado por la constante enumerada, **adSchemaColumns**, está asociado a cuatro columnas de restricción:\_el catálogo de\_tablas,\_el esquema de la tabla\_, el nombre de la tabla y el nombre de la columna. Por lo tanto, se crea una matriz de valores **Variant** con cuatro elementos. A continuación, se especifica un valor de restricción que corresponde a\_la tercera columna, nombre de tabla. El objeto **Recordset** que se devuelve consta de varias columnas, entre las que se incluyen las columnas de restricción. Los valores de las columnas de restricción para cada fila devuelta deben ser los mismos que los valores de restricción correspondientes.

4. Aquéllos familiarizados con **SafeArrays** se pueden sorprender del hecho de que no se llame a **SafeArrayDestroy**() antes de la salida. De hecho, llamar a **SafeArrayDestroy**() provocará en este caso una excepción en tiempo de ejecución. El motivo es que el destructor de vtCriteria llamará a **VariantClear**() cuando ** \_Variant\_t** se salga del ámbito, lo que liberará **SAFEARRAY**. La llamada a **SafeArrayDestroy**, sin borrar manualmente la ** \_\_variante t**, haría que el destructor intentara borrar un puntero **SAFEARRAY** no válido. Si se hiciera la llamada a **SafeArrayDestroy**, el código presentaría el siguiente aspecto:
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Sin embargo, es mucho más sencillo permitir que la ** \_Variant\_t** administre **SAFEARRAY**.


```cpp 
 
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
    
    // Note 1 
    inline void TESTHR( HRESULT _hr ) 
    { if FAILED(_hr) _com_issue_error(_hr); } 
    
    void main(void) 
    { 
    CoInitialize(NULL); 
    try 
    { 
    _RecordsetPtr pRs("ADODB.Recordset"); 
    _ConnectionPtr pCn("ADODB.Connection"); 
    _variant_t vtTableName("authors"), 
    vtCriteria; 
    long ix[1]; 
    SAFEARRAY *pSa = NULL; 
    
    pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
    adConnectUnspecified); 
    // Note 2, Note 3 
    pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
    if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
    
    // Specify TABLE_NAME in the third array element (index of 2). 
    
    ix[0] = 2; 
    TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
    
    // There is no Variant constructor for a SafeArray, so manually set the 
    // type (SafeArray of Variant) and value (pointer to a SafeArray). 
    
    vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
    vtCriteria.parray = pSa; 
    
    pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
    
    long limit = pRs->GetFields()->Count; 
    for (long x = 0; x < limit; x++) 
    printf("%d: %s\n", x+1, 
    ((char*) pRs->GetFields()->Item[x]->Name)); 
    // Note 4 
    pRs->Close(); 
    pCn->Close(); 
    } 
    catch (_com_error &e) 
    { 
    printf("Error:\n"); 
    printf("Code = %08lx\n", e.Error()); 
    printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
    printf("Source = %s\n", (char*) e.Source()); 
    printf("Description = %s\n", (char*) e.Description()); 
    } 
    CoUninitialize(); 
    } 
```

### <a name="using-property-getputputref"></a>Uso de la propiedad Get/Put/PutRef

En Visual Basic, el nombre de una propiedad no indica si ésta se ha recuperado, si se le ha asignado un valor o se le ha asignado una referencia.

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

En este ejemplo de Visual C++ se muestra la propiedad **Get**/**Put**/**PutRef * * **.

> [!NOTE]
> Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.

1. En este ejemplo se usan dos formas de un argumento de cadena que falta: una constante explícita, **strMissing**, y una cadena que el compilador va a usar para crear un ** \_\_BSTR t** temporal que existirá para el ámbito del método **Open** .

2. No es necesario convertir el operando de RS-\>PutRefActiveConnection (CN) a (IDispatch \*), ya que el tipo del operando ya es \*(IDispatch).
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="using-getitemx-and-itemx"></a>Usar GetItem (x) e Item\[x\]

Este ejemplo de Visual Basic muestra la sintaxis estándar y alternativa para **Item**().

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

En este ejemplo de Visual C++, se muestra el uso de **Item**.

> [!NOTE]
> [!NOTA] La nota siguiente corresponde a secciones comentadas en el ejemplo de código.

1. Cuando se obtiene acceso a la colección mediante **Item**, el índice, **2**, se debe convertir explícitamente a **long** para que se realice la llamada al constructor apropiado.
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Conversión de punteros a objetos ADO con \*(IDispatch)

El siguiente ejemplo de Visual C++ muestra el uso de ( IDispatch \* ) para convertir explícitamente punteros a objetos ADO.

> [!NOTE]
> [!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.

1. Especifique un objeto **Connection** abierto en un **Variant** codificado explícitamente. Conviértalo en (IDispatch \*) para que se invoque el constructor correcto. Además, establezca explícitamente el ** \_segundo\_parámetro Variant t** en el valor predeterminado de **true**, de modo que el recuento de referencias de objeto será correcto cuando finalice la operación **Recordset:: Open** .

2. La expresión\_(BSTR\_t) no es una conversión explícita, sino un ** \_operador Variant\_t** que extrae una ** \_cadena BSTR\_t** de la **variante** devuelta por **Value**. La expresión (char\*) no es una conversión explícita, sino un ** \_operador BSTR\_t** que extrae un puntero a la cadena encapsulada en un ** \_objeto\_BSTR t** . En esta sección de código se muestran algunos de los comportamientos ** \_útiles\_** de los operadores Variant t y ** \_BSTR\_t** .
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
   ```

