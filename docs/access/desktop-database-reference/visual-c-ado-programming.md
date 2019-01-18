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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721293"
---
# <a name="visual-c-ado-programming"></a>Programación de ADO con Visual C++

**Se aplica a**: Access 2013, Office 2013

La Referencia de la API de ADO describe la funcionalidad de la interfaz de programación de aplicaciones (API) de ADO mediante una sintaxis similar a Microsoft Visual Basic. Aunque los destinatarios son todos los usuarios, los programadores de ADO emplean diversos lenguajes como Visual Basic, Visual C++ (con y sin el ** \#importar** directiva) y Visual J ++ (con el paquete de clases ADO/WFC).

Para dar cabida a esta diversidad, los [Índices de sintaxis de ADO para Visual C++](using-ado-with-microsoft-visual-c.md) proporcionan sintaxis específica de Visual C++ con vínculos a descripciones comunes de funcionalidad, parámetros, comportamientos excepcionales, etc., en la Referencia de la API.

ADO se implementa con interfaces COM (Modelo de objetos componentes). Sin embargo, es más fácil para los programadores trabajar con COM en algunos lenguajes de programación que en otros. Por ejemplo, casi todos los detalles del uso de COM se manejan implícitamente en Visual Basic, mientras que en Visual C++ son los programadores quienes deben manejar esos detalles.

En las secciones siguientes resumen la información para los programadores de C y C++ que utilizan ADO y la ** \#importar** directiva. Se centra en tipos de datos específicos de COM (**Variant**, **BSTR**y **SafeArray**) y tratamiento de errores (\_com\_error).

## <a name="using-the-import-compiler-directive"></a>Uso de la \#Importar directiva del compilador

La ** \#importar** directiva del compilador de Visual C++ simplifica el trabajo con las propiedades y métodos de ADO. La directiva toma el nombre de un archivo que contiene una biblioteca de tipos, tal como la dll de ADO (Msado15.dll), y genera archivos de encabezado que contienen declaraciones typedef, punteros inteligentes para interface y constantes enumeradas. Cada interfaz se encapsula o engloba en una clase.

Para cada operación dentro de una clase (es decir una llamada a método o propiedad), existe una declaración para llamar a la operación directamente (es decir, la forma "original" de la operación) y una declaración para llamar a la operación original y generar un error COM si la operación no se ejecuta correctamente. Si la operación es una propiedad, suele existir una directiva del compilador que crea una sintaxis alternativa para la operación que tiene sintaxis similar a Visual Basic.

Las operaciones que recuperan el valor de una propiedad tienen nombres de la forma, **obtener *** (propiedad)*. Las operaciones que establezca el valor de una propiedad tienen nombres de la forma, **colocar *** (propiedad)*. Las operaciones que establecen el valor de una propiedad con un puntero a un objeto ADO tienen nombres de la forma, **PutRef *** (propiedad)*.

Puede obtener o establecer una propiedad con llamadas de este tipo:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Utilizar directivas de propiedad

La ** \_ \_declspec(property...)** directiva del compilador es una extensión del lenguaje C específica de Microsoft que declara una función utilizada como una propiedad que tenga una sintaxis alternativa. Como resultado, puede establecer u obtener valores de una propiedad de forma similar a Visual Basic. Por ejemplo, puede establecer y obtener una propiedad de este modo:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Tenga en cuenta que no tiene que escribir este código:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

El compilador generará la adecuada **Get ***-*, **Put**-, o **PutRef *** (propiedad)* llamada según la sintaxis alternativa declarada y si la propiedad se va a leer o escribir.

La ** \_ \_declspec(property...)** directiva del compilador sólo puede declarar **get**, **put**o **get** y **put** sintaxis alternativa para una función. Las operaciones de solo lectura sólo tienen una declaración **get** ; operaciones de sólo escritura únicamente tienen una declaración **put** ; las operaciones que son de lectura y escritura tienen declaraciones **get** y **put** .

Sólo hay dos declaraciones son posibles con esta directiva; Sin embargo, cada propiedad tiene tres funciones: **obtener *** (propiedad)*, **colocar *** (propiedad)*, y **PutRef *** (propiedad)*. En ese caso, sólo dos formas de la propiedad presentan sintaxis alternativa.

Por ejemplo, la propiedad **ActiveConnection** del objeto **Command** se declara con una sintaxis alternativa para **obtener *** ActiveConnection* y **PutRef *** ActiveConnection*. **PutRef**- sintaxis es una buena opción debido a que en la práctica, normalmente desean colocar un objeto **Connection** abierto (es decir, un puntero de objeto de **conexión** ) en esta propiedad. Por otro lado, el objeto **Recordset** tiene **Get**-, **Put**-, y **PutRef *** ActiveConnection* las operaciones, pero sin sintaxis alternativa.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Colecciones, el método GetItem y la propiedad Item

ADO define varias colecciones, incluidas **Fields**, **Parameters**, **Properties** y **Errors**. En Visual C++, el método **GetItem(***índice***)** devuelve un miembro de la colección. *Índice* es de un tipo **Variant**, cuyo valor es el índice numérico del miembro de la colección o una cadena que contiene el nombre del miembro.

La ** \_ \_declspec(property...)** directiva del compilador declara la propiedad **Item** como una sintaxis alternativa al método **GetItem()** fundamental de cada colección. La sintaxis alternativa utiliza corchetes y es similar a una referencia a matriz. En general, las dos formas son similares a lo siguiente:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Por ejemplo, asignar un valor a un campo de un objeto **Recordset** , denominado ***rs***, derivado de la tabla **authors** de la base de datos **pubs** . Utilice la propiedad **Item()** para obtener acceso al tercer **campo** de la colección **Fields** del objeto **Recordset** (las colecciones se indizan desde cero; suponga que el tercer campo se denomina ***au\_fname***). A continuación, llame al método **Value()** sobre el objeto **Field** para asignar un valor de tipo string.

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

\-o -(también se muestra la sintaxis alternativa de la propiedad **Value** )

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Tipos de datos específicos de COM

En general, cualquier tipo de datos de Visual Basic que se encuentra en la Referencia de la API de ADO tiene un equivalente en Visual C++. Éstos incluyen tipos de datos estándar, tales como **unsigned char** para un **Byte** de Visual Basic, **short** para **Integer** y **long** para **Long**. Busque en los Índices de la sintaxis para ver qué se requiere exactamente para los operandos de un método o una propiedad dados.

Las excepciones a esta regla son los tipo de datos específicos de COM: **Variant**, **BSTR** y **SafeArray**.

### <a name="variant"></a>Variant

Un **Variant** es un tipo de datos estructurados que contiene un miembro de valor y un miembro de tipo de datos. Un **Variant** puede contener una amplia variedad de otros tipos de datos, incluidos otro Variant, BSTR, Boolean, IDispatch, puntero a IUnknown, moneda, fecha, etc. COM también proporciona métodos que facilitan la conversión de un tipo de datos en otro.

La ** \_variant\_t** clase encapsula y administra el tipo de datos **Variant** .

Cuando la referencia de API de ADO indica que un método u operando propiedad toma un valor, suele significar que el valor se pasa en un ** \_variant\_t**.

Esta regla se cumple explícitamente cuando la sección **Parámetros** de los temas de la Referencia de la API de ADO indica que un operando es de tipo **Variant**. Una excepción es cuando la documentación indica explícitamente que el operandos toma un tipo de datos estándar, como **Long**, **Byte** o una enumeración. Otra excepción es cuando el operando toma un **String**.

### <a name="bstr"></a>BSTR

Un **BSTR** (**B**asic **STR**ing) es un tipo de datos estructurados que contiene una cadena de caracteres y la longitud de la cadena. COM proporciona métodos para asignar, manipular y liberar un **BSTR**.

La ** \_bstr\_t** clase encapsula y administra el tipo de datos **BSTR** .

Cuando la referencia de API de ADO indica que un método o una propiedad toman un valor de **tipo String** , significa que el valor se encuentra en el formulario de un ** \_bstr\_t**.

#### <a name="casting-variantt-and-bstrt-classes"></a>Convirtiendo \_variant\_t y \_bstr\_clases t

A menudo no es necesario para el código de forma explícita una ** \_variant\_t** o ** \_bstr\_t** en un argumento para una operación. Si el ** \_variant\_t** o ** \_bstr\_t** clase tiene un constructor que coincide con el tipo de datos del argumento, a continuación, el compilador generará la adecuada ** \_variant\_t** o ** \_ BSTR\_t**.

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

El argumento ActiveConnection acepta una referencia a un ** \_variant\_t**, que se puede codificar como una cadena de conexión o un puntero a un objeto **Connection** abierto.

La correcta ** \_variant\_t** se construirá implícitamente si se pasa una cadena tal como "DSN = pubs; uid = sa; pwd =;", o un puntero tal como "(IDispatch \*) pConn".

O bien, puede codificar explícitamente un ** \_variant\_t** que contiene un puntero tal como "\_variant\_t ((IDispatch \*) pConn, true)". La conversión explícita, (IDispatch \*), resuelve la ambigüedad con otro constructor que toma un puntero a una interfaz IUnknown.

Es un hecho crucial (aunque raramente mencionado) que ADO es una interfaz IDispatch. Siempre que un puntero a un objeto ADO se deba pasar como un **Variant**, es necesario convertir explícitamente ese puntero a un puntero a un interfaz IDispatch.

El último caso codifica explícitamente el segundo argumento booleano del constructor con su valor predeterminado opcional true. Este argumento hace que el constructor de **tipo Variant** llamar al método **AddRef**(), que compensa a ADO automáticamente llamando el ** \_variant\_t::Release**(método) () una vez completada la llamada al método o propiedad de ADO.

### <a name="safearray"></a>SafeArray

Un **SafeArray** es un tipo de datos estructurados que contiene una matriz de otros tipos de datos. Un **SafeArray** se denomina *seguros* porque contiene información acerca de los límites de cada dimensión de la matriz y limita el acceso a elementos de la matriz a esos límites.

Cuando la Referencia de la API de ADO indica que un método o una propiedad acepta o devuelve una matriz, significa que el método o la propiedad acepta o devuelve un **SafeArray** no una matriz nativa de C/C++.

Por ejemplo, el segundo parámetro del método **OpenSchema** del objeto **Conection** requiere una matriz de valores **Variant**. Esos valores **Variant** se deben pasar como elementos de un **SafeArray**, y ese **SafeArray** se debe establecer como el valor de otro **Variant**. Es ese otro **Variant** el que se pasa como el segundo argumento de **OpenSchema**.

Como ejemplos adicionales, el primer argumento del método **Find** es un **Variant** cuyo valor es un **SafeArray** unidimensional, cada uno de los argumentos primero y segundo opcionales de **AddNew** es un **SafeArray** unidimensional y el valor devuelto del método **GetRows** es un **Variant** cuyo valor es un **SafeArray** bidimensional.

## <a name="missing-and-default-parameters"></a>Parámetros predeterminados y ausentes

Visual Basic permite que falten parámetros en los métodos. Por ejemplo, el método **Open** de un objeto **Recordset** tiene cinco parámetros, pero se pueden omitir parámetros intermedios y no incluir parámetros finales. Se usará entonces un **BSTR** o **Variant** predeterminado según el tipo de datos del operando que falte.

En C/C++, se deben especificar todos los operandos. Si desea especificar un parámetro que falta cuyo tipo de datos es una cadena, especifique un ** \_bstr\_t** que contenga una cadena nula. Si desea especificar un parámetro que falta cuyo tipo de datos es un **tipo Variant**, especifique un ** \_variant\_t** con un valor de DISP\_E\_PARAMNOTFOUND y un tipo de VT\_ERROR. Como alternativa, especifique el equivalente ** \_variant\_t** constante, **vtMissing**, que es proporcionado por el ** \#importar** directiva.

Existen tres métodos que constituyen excepciones al uso típico de **vtMissing**. Éstos son los métodos **Execute** de los objetos **Connection** y **Command**, y el método **NextRecordset** del objeto **Recordset**. Las siguientes son sus firmas:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Los parámetros *RecordsAffected* y *Parameters*son punteros a un **Variant**. *Parameters* es un parámetro de entrada que especifica la dirección de un **Variant** que contiene un parámetro único, o una matriz de parámetros, que modificará el comando que se va a ejecutar. *RecordsAffected* es un parámetro de salida que especifica la dirección de un **Variant** donde se devuelve el número de filas afectadas por el método.

En el método **Execute** del **comando** objeto, indique que se ha especificado ningún parámetro estableciendo *parámetros* en cualquiera \&vtMissing (que se recomienda) o como el puntero nulo (es decir, **NULL** o cero (0)). Si *los parámetros* se establece como el puntero nulo, el método sustituye internamente el equivalente de **vtMissing**y, a continuación, completa la operación.

En todos los métodos, indique que no se debe devolver el número de registros afectados estableciendo *RecordsAffected* como el puntero nulo. En este caso, el puntero nulo no es tanto un parámetro que falta como una indicación de que el método debería descartar el número de registros afectados.

Por tanto, para estos tres métodos, es correcto codificar del siguiente modo:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Control de errores

En COM, la mayoría de las operaciones devolverá un código de retorno HRESULT que indica si una función se completó correctamente. La ** \#importar** directiva genera código contenedor alrededor de cada método "sin procesar" o la propiedad y comprueba el HRESULT devuelto. Si el HRESULT indica error, el código de contenedor genera un error COM llamando a \_com\_problema\_errorex() con el HRESULT devolver código como un argumento. Objetos de error COM se pueden capturar en **probar**-bloque**catch** . (Para una mayor eficacia, detecte una referencia a un ** \_com\_error** objeto.)

Recuerde que éstos son errores de ADO (resultado de una operación ADO). Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.

La ** \#importar** directiva sólo crea errores rutinas de tratamiento de los métodos y propiedades declaradas en la DLL de ADO. Sin embargo, puede aprovechar este mismo mecanismo de tratamiento de errores escribiendo su propia función en línea o macro de comprobación de errores. Vea el tema [Extensiones de Visual C++](visual-c-extensions-for-ado.md) o el código de la sección siguiente para obtener ejemplos.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Equivalentes Visual C++ de las convenciones de Visual Basic

A continuación, se muestra un resumen de diversas convenciones de la documentación de ADO, codificadas en Visual Basic, así como sus equivalentes en Visual C++.

### <a name="declaring-an-ado-object"></a>Declaración de un objeto ADO

En Visual Basic, una variable de objeto ADO (en este caso, de un objeto **Recordset** ) se declara del siguiente modo:

```vb 
 
Dim rst As ADODB.Recordset 
```

La cláusula "ADODB. Objeto Recordset"es el ProgID del objeto **Recordset** tal como se define en el registro. Una instancia nueva de un objeto **Record** se declara del siguiente modo:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-o -

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

En Visual C++, la ** \#importar** directiva genera declaraciones de tipo puntero inteligente para todos los objetos de ADO. Por ejemplo, una variable que apunta a un ** \_Recordset** objeto es del tipo ** \_RecordsetPtr**y se declara del siguiente modo:

```cpp 
 
_RecordsetPtr rs; 
```

Una variable que apunta a una nueva instancia de un ** \_Recordset** objeto se declara del siguiente modo:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-o -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-o -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

Después de llamar al método **CreateInstance**, la variable se puede utilizar de la manera siguiente:

```cpp 
 
rs->Open(...); 
```

Tenga en cuenta que en un caso, el "." se usa el operador como si la variable fuera una instancia de una clase (rs. CreateInstance) y en otro caso, el "-\>" se usa el operador como si la variable fuera un puntero a una interfaz (rs -\>Open).

Una variable se puede utilizar de dos maneras debido a que la "-\>" operador está sobrecargado para permitir que una instancia de una clase que se comporte como un puntero a una interfaz. Un miembro privado de clase de la variable de instancia contiene un puntero a la ** \_Recordset** de la interfaz; la "-\>" operador devuelve ese puntero; y el puntero devuelto obtiene acceso a los miembros de la ** \_Recordset** objeto.

### <a name="coding-a-missing-parameter"></a>Codificar un parámetro que falta

#### <a name="string"></a>String

Cuando necesite codificar en Visual Basic un operando **String** ausente, simplemente omita el operando. Deberá especificar el operando en Visual C++. Código un ** \_bstr\_t** que tiene una cadena vacía como un valor.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

Cuando necesite codificar en Visual Basic un operando **Variant** ausente, simplemente omita el operando. En Visual C++, deberá especificar todos los operandos. Codifique un parámetro **Variant** ausente con un ** \_variant\_t** establecida en el valor especial, DISP\_E\_PARAMNOTFOUND y tipo, VT\_ERROR. Como alternativa, especifique **vtMissing**, que es equivalente a un constante predefinido proporcionados por la ** \#importar** directiva.

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-o utilice-

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Declaración de un variant

En Visual Basic, un tipo **Variant** se declara con la instrucción **Dim** del siguiente modo:

```vb 
 
Dim VariableName As Variant 
```

En Visual C++, declare una variable como tipo de ** \_variant\_t**. Esquema unos ** \_variant\_t** declaraciones se muestran a continuación.

> [!NOTE]
> [!NOTA] Estas declaraciones simplemente proporcionan una idea general de cómo podría codificar su propio programa. Para obtener más información, vea los ejemplos siguientes y la documentación de Visual C++.

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>Uso de matrices de variants

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

El siguiente ejemplo de Visual C++ muestra cómo utilizar un **SafeArray** con un ** \_variant\_t**.

> [!NOTE]
> [!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.

1. Una vez más, se define la función inline TESTHR() para aprovechar el mecanismo de control de errores existente.

2. Sólo necesitará una matriz unidimensional, de forma que pueda utilizar **SafeArrayCreateVector** en lugar de la declaración de propósito general **SAFEARRAYBOUND** y la función **SafeArrayCreate**. El código que utiliza **SafeArrayCreate** tiene el siguiente aspecto:
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. El esquema identificado por la constante enumerada **adSchemaColumns**se asocia con cuatro columnas de restricción: tabla\_catálogo, tabla\_esquema, tabla\_nombre y columna\_nombre. Por lo tanto, se crea una matriz de valores **Variant** con cuatro elementos. A continuación, un valor de restricción que corresponde a la tercera columna, tabla\_nombre, se ha especificado. El objeto **Recordset** que se devuelve consta de varias columnas, entre las que se incluyen las columnas de restricción. Los valores de las columnas de restricción para cada fila devuelta deben ser los mismos que los valores de restricción correspondientes.

4. Aquellos que estén familiarizados con **SAFEARRAY** se sorprendan que no se llama a **SafeArrayDestroy**() antes de la salida. De hecho, llamar a **SafeArrayDestroy**() provocará en este caso una excepción de tiempo de ejecución. La razón es que el destructor de vtCriteria llamará a () **VariantClear**cuando la ** \_variant\_t** queda fuera del ámbito, lo que liberará el **SafeArray**. La llamada a **SafeArrayDestroy**, sin borrar manualmente el ** \_variant\_t**, hará que el destructor intente borrar un puntero **SafeArray** no válido. Si se hiciera la llamada a **SafeArrayDestroy**, el código presentaría el siguiente aspecto:
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Sin embargo, resulta más sencillo permitir que el ** \_variant\_t** administre el **SafeArray**.


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

### <a name="using-property-getputputref"></a>Uso de Get/Put/PutRef propiedad

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

En este ejemplo de Visual C++ muestra cómo **obtener**/**colocar**/**PutRef *** (propiedad)*.

> [!NOTE]
> [!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.

1. En este ejemplo se utiliza dos formas de un argumento de cadena que falta: una constante explícita, **strMissing**y una cadena que el compilador utilizará para crear un archivo temporal ** \_bstr\_t** que existirá durante el ámbito del método **Open** .

2. No es necesario convertir explícitamente el operando de rs -\>PutRefActiveConnection a (IDispatch \*) porque el tipo del operando es ya (IDispatch \*).
    
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

### <a name="using-getitemx-and-itemx"></a>Utilizar GetItem y elemento\[x\]

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

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Convertir explícitamente punteros a objetos ADO con ( IDispatch \* )

El siguiente ejemplo de Visual C++ muestra el uso de ( IDispatch \* ) para convertir explícitamente punteros a objetos ADO.

> [!NOTE]
> [!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.

1. Especifique un objeto **Connection** abierto en un **Variant** codificado explícitamente. Conviértalo explícitamente con (IDispatch \*) por lo que se invocará el constructor correcto. Además, establezca explícitamente el segundo ** \_variant\_t** parámetro para el valor predeterminado **es true**, por lo que el recuento de referencia de objeto será correcto cuando termina la operación **Recordset:: Open** .

2. La expresión (\_bstr\_t), no es una conversión de tipos, pero un ** \_variant\_t** operador que extrae una ** \_bstr\_t** cadena del **tipo Variant** devuelto por **valor**. La expresión (char\*), no es una conversión de tipos, pero un ** \_bstr\_t** operador que extrae un puntero a la cadena encapsulado en un ** \_bstr\_t** objeto. En esta sección de código, se muestra algunos de los comportamientos útiles de ** \_variant\_t** y ** \_bstr\_t** operadores.
    
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

