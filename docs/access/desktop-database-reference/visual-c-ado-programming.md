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

La Referencia de la API de ADO describe la funcionalidad de la interfaz de programación de aplicaciones (API) de ADO mediante una sintaxis similar a Microsoft Visual Basic. Aunque la audiencia prevista es de todos los usuarios, los programadores de ADO emplean varios idiomas, como Visual Basic, Visual C++ (con y sin la directiva **\# de** importación) y Visual J++ (con el paquete de clase ADO/WFC).

Para dar cabida a esta diversidad, los [Índices de sintaxis de ADO para Visual C++](using-ado-with-microsoft-visual-c.md) proporcionan sintaxis específica de Visual C++ con vínculos a descripciones comunes de funcionalidad, parámetros, comportamientos excepcionales, etc., en la Referencia de la API.

ADO se implementa con interfaces COM (Modelo de objetos componentes). Sin embargo, es más fácil para los programadores trabajar con COM en algunos lenguajes de programación que en otros. Por ejemplo, casi todos los detalles del uso de COM se manejan implícitamente en Visual Basic, mientras que en Visual C++ son los programadores quienes deben manejar esos detalles.

En las secciones siguientes se resumen los detalles para programadores de C y C++ mediante ADO y la **\# directiva de** importación. Se centra en tipos de datos específicos de COM (**Variant**, **BSTR** y **SafeArray**) y control de errores ( \_ error \_ com).

## <a name="using-the-import-compiler-directive"></a>Uso de \# la directiva del compilador de importación

La **\# directiva del** compilador de Importación de Visual C++ simplifica el trabajo con los métodos y propiedades de ADO. La directiva toma el nombre de un archivo que contiene una biblioteca de tipos, tal como la dll de ADO (Msado15.dll), y genera archivos de encabezado que contienen declaraciones typedef, punteros inteligentes para interface y constantes enumeradas. Cada interfaz se encapsula o engloba en una clase.

Para cada operación dentro de una clase (es decir una llamada a método o propiedad), existe una declaración para llamar a la operación directamente (es decir, la forma "original" de la operación) y una declaración para llamar a la operación original y generar un error COM si la operación no se ejecuta correctamente. Si la operación es una propiedad, suele existir una directiva del compilador que crea una sintaxis alternativa para la operación que tiene sintaxis similar a Visual Basic.

Las operaciones que recuperan el valor de una propiedad tienen nombres del formulario, **Get***Property*. Las operaciones que establecen el valor de una propiedad tienen nombres del formulario, **Put***Property*. Las operaciones que establecen el valor de una propiedad con un puntero a un objeto ADO tienen nombres del formulario, **PutRef***Property*.

Puede obtener o establecer una propiedad con llamadas de este tipo:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Uso de directivas de propiedades

La directiva del compilador **\_ \_ declspec(property...)** es una extensión de lenguaje C específica de Microsoft que declara una función usada como propiedad para tener una sintaxis alternativa. Como resultado, puede establecer u obtener valores de una propiedad de forma similar a Visual Basic. Por ejemplo, puede establecer y obtener una propiedad de este modo:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Tenga en cuenta que no tiene que escribir este código:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

El compilador generará la llamada adecuada **Get***-*, **Put**-, o **PutRef***Property* en función de la sintaxis alternativa que se declara y de si la propiedad se lee o escribe.

La **\_ \_ directiva del compilador declspec(property...)** solo  puede declarar **obtener,** **poner** o obtener y poner una **sintaxis** alternativa para una función. Las operaciones de sólo lectura únicamente tienen una declaración **get**; las operaciones de sólo escritura únicamente tienen una declaración **put**; las operaciones de lectura y escritura tienen ambas declaraciones **get** y **put**.

Solo son posibles dos declaraciones con esta directiva; sin embargo, cada propiedad puede tener tres funciones de propiedad: **Get***Property*, **Put***Property* y **PutRef***Property*. En ese caso, sólo dos formas de la propiedad presentan sintaxis alternativa.

Por ejemplo, la **propiedad Command** del objeto **ActiveConnection** se declara con una sintaxis alternativa para **Get***ActiveConnection* y **PutRef***ActiveConnection*. La sintaxis de **PutRef** constituye una buena elección, ya que, en la práctica, deseará establecer un objeto **Connection** abierto (es decir, un puntero a un objeto **Connection**) en esta propiedad. Por otro lado, el **objeto Recordset** tiene operaciones **Get**-, **Put**-, y **PutRef***ActiveConnection,* pero sin sintaxis alternativa.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Colecciones, el método GetItem y la propiedad Item

ADO define varias colecciones, incluidas **Fields**, **Parameters**, **Properties** y **Errors**. En Visual C++, el **método GetItem(***index***)** devuelve un miembro de la colección. *Índice* es de un tipo **Variant**, cuyo valor es el índice numérico del miembro de la colección o una cadena que contiene el nombre del miembro.

La directiva del compilador **\_ \_ declspec(property...)** declara la **propiedad Item** como una sintaxis alternativa al método **getitem()** fundamental de cada colección. La sintaxis alternativa utiliza corchetes y es similar a una referencia a matriz. En general, las dos formas son similares a lo siguiente:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Por ejemplo, asigne un valor a un campo de un objeto **Recordset**, denominado ***rs***, derivado de la tabla **authors** de la base de datos **pubs**. Utilice la **propiedad Item()** para obtener acceso al tercer **campo** de la colección **Fields** del objeto **Recordset** (las colecciones se indizan desde cero; suponga que el tercer campo se denomina ***au \_ fname***). A continuación, llame al método **Value()** sobre el objeto **Field** para asignar un valor de cadena.

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

\-o- (también se muestra la sintaxis alternativa para **la propiedad Value)**

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Tipos de datos específicos de COM

En general, cualquier tipo de datos de Visual Basic que se encuentra en la Referencia de la API de ADO tiene un equivalente en Visual C++. Éstos incluyen tipos de datos estándar, tales como **unsigned char** para un **Byte** de Visual Basic, **short** para **Integer** y **long** para **Long**. Busque en los Índices de la sintaxis para ver qué se requiere exactamente para los operandos de un método o una propiedad dados.

Las excepciones a esta regla son los tipo de datos específicos de COM: **Variant**, **BSTR** y **SafeArray**.

### <a name="variant"></a>Variant

Un **Variant** es un tipo de datos estructurados que contiene un miembro de valor y un miembro de tipo de datos. Un **Variant** puede contener una amplia variedad de otros tipos de datos, incluidos otro Variant, BSTR, Boolean, IDispatch, puntero a IUnknown, moneda, fecha, etc. COM también proporciona métodos que facilitan la conversión de un tipo de datos en otro.

La **\_ clase variant \_ t** encapsula y administra el tipo de datos **Variant.**

Cuando la referencia de api de ADO indica que un operando de método o propiedad toma un valor, normalmente significa que el valor se pasa en **\_ una variante \_ t**.

Esta regla se cumple explícitamente cuando la sección **Parámetros** de los temas de la Referencia de la API de ADO indica que un operando es de tipo **Variant**. Una excepción es cuando la documentación indica explícitamente que el operandos toma un tipo de datos estándar, como **Long**, **Byte** o una enumeración. Otra excepción es cuando el operando toma un **String**.

### <a name="bstr"></a>BSTR

Un **BSTR** (**B** asic **STR** ing) es un tipo de datos estructurados que contiene una cadena de caracteres y la longitud de la cadena. COM proporciona métodos para asignar, manipular y liberar un **BSTR**.

La **\_ clase bstr \_ t** encapsula y administra el **tipo de datos BSTR.**

Cuando la referencia de api de ADO indica que un método o propiedad toma un valor **string,** significa que el valor está en forma de **\_ bstr \_ t**.

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a>Conversión \_ de clases variant t y \_ \_ bstr \_ t

A menudo no es necesario codificar explícitamente una **\_ variante \_ t** o **\_ bstr \_ t** en un argumento a una operación. Si la **\_ clase variant \_ t** o **\_ bstr \_ t** tiene un constructor que coincide con el tipo de datos del argumento, el compilador generará la variante **\_ \_ t** o **\_ bstr \_ t apropiadas.**

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

El argumento ActiveConnection hace referencia a una variante **\_ \_ t**, que puede codificar como una cadena de conexión o un puntero a un **objeto Connection** abierto.

La variante **\_ \_ correcta t** se construirá implícitamente si pasa una cadena como "DSN=pubs;uid=sa;pwd=;", o un puntero como "(IDispatch ) \* pConn".

O puede codificar explícitamente una variante **\_ \_ que** contenga un puntero como " \_ variant \_ t((IDispatch \* ) pConn, true)". La conversión ( IDispatch ), resuelve la ambigüedad con otro constructor que toma un \* puntero a una interfaz IUnknown.

Es un hecho crucial (aunque raramente mencionado) que ADO es una interfaz IDispatch. Siempre que un puntero a un objeto ADO se deba pasar como un **Variant**, es necesario convertir explícitamente ese puntero a un puntero a un interfaz IDispatch.

El último caso codifica explícitamente el segundo argumento booleano del constructor con su valor predeterminado opcional true. Este argumento hace que el constructor **Variant** llame a su **método AddRef**(), que compensa la llamada automática de ADO al método **\_ variant \_ t::Release**() cuando se completa el método ADO o la llamada a la propiedad.

### <a name="safearray"></a>SafeArray

Un **SafeArray** es un tipo de datos estructurados que contiene una matriz de otros tipos de datos. Un **SafeArray** se denomina *safe* (seguro) debido a que contiene información sobre los límites de cada dimensión de la matriz y limita el acceso a los elementos de la matriz a esos límites.

Cuando la Referencia de la API de ADO indica que un método o una propiedad acepta o devuelve una matriz, significa que el método o la propiedad acepta o devuelve un **SafeArray** no una matriz nativa de C/C++.

Por ejemplo, el segundo parámetro del método **OpenSchema** del objeto **Conection** requiere una matriz de valores **Variant**. Esos valores **Variant** se deben pasar como elementos de un **SafeArray**, y ese **SafeArray** se debe establecer como el valor de otro **Variant**. Es ese otro **Variant** el que se pasa como el segundo argumento de **OpenSchema**.

Como ejemplos adicionales, el primer argumento del método **Find** es un **Variant** cuyo valor es un **SafeArray** unidimensional, cada uno de los argumentos primero y segundo opcionales de **AddNew** es un **SafeArray** unidimensional y el valor devuelto del método **GetRows** es un **Variant** cuyo valor es un **SafeArray** bidimensional.

## <a name="missing-and-default-parameters"></a>Parámetros faltantes y predeterminados

Visual Basic permite que falten parámetros en los métodos. Por ejemplo, el método **Open** de un objeto **Recordset** tiene cinco parámetros, pero se pueden omitir parámetros intermedios y no incluir parámetros finales. Se usará entonces un **BSTR** o **Variant** predeterminado según el tipo de datos del operando que falte.

En C/C++, se deben especificar todos los operandos. Si desea especificar un parámetro que falta cuyo tipo de datos es una cadena, especifique un **\_ bstr \_ t** que contenga una cadena nula. Si desea especificar un parámetro que falta cuyo tipo de datos es **Variant**, especifique una variante **\_ \_ t** con un valor de DISP \_ E PARAMNOTFOUND y un tipo \_ de ERROR \_ VT. Como alternativa, especifique la constante **\_ \_ t de** variante equivalente, **vtMissing**, que proporciona la directiva **\# de** importación.

Existen tres métodos que constituyen excepciones al uso típico de **vtMissing**. Éstos son los métodos **Execute** de los objetos **Connection** y **Command**, y el método **NextRecordset** del objeto **Recordset**. Las siguientes son sus firmas:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Los parámetros *RecordsAffected* y *Parameters* son punteros a un **Variant**. *Parameters* es un parámetro de entrada que especifica la dirección de un **Variant** que contiene un parámetro único, o una matriz de parámetros, que modificará el comando que se va a ejecutar. *RecordsAffected* es un parámetro de salida que especifica la dirección de un **Variant** donde se devuelve el número de filas afectadas por el método.

En el **método Execute** del objeto **Command,** indique que no se especifica ningún parámetro estableciendo *Parameters* en vtMissing (que se recomienda) o en el puntero \& nulo (es decir, **NULL** o cero (0)). Si *Parameters* se establece en el puntero nulo, el método sustituye internamente el equivalente de **vtMissing** y, a continuación, completa la operación.

En todos los métodos, indique que no se debe devolver el número de registros afectados; puede hacerlo estableciendo *RecordsAffected* en un puntero nulo. En este caso, el puntero nulo no es tanto un parámetro que falta como una indicación de que el método debería descartar el número de registros afectados.

Por tanto, para estos tres métodos, es correcto codificar del siguiente modo:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Control de errores

In COM, most operations return an HRESULT return code that indicates whether a function completed successfully. La **\# directiva import** genera código contenedor alrededor de cada método o propiedad "sin procesar" y comprueba el HRESULT devuelto. Si el HRESULT indica un error, el código contenedor genera un error COM llamando a \_ \_ com issue errorex() con el código devuelto \_ HRESULT como argumento. COM error objects can be caught in a **try**-**catch** block. (Por razones de eficiencia, captura una referencia a un **\_ objeto de \_ error com).**

Recuerde que éstos son errores de ADO (resultado de una operación ADO). Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.

La **\# directiva import** crea solo rutinas de control de errores para métodos y propiedades declarados en el .dll ADO. Sin embargo, puede aprovechar este mismo mecanismo de tratamiento de errores escribiendo su propia función en línea o macro de comprobación de errores. Vea el tema [Extensiones de Visual C++](visual-c-extensions-for-ado.md) o el código de la sección siguiente para obtener ejemplos.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Equivalentes de Visual C++ de Visual Basic convenciones

A continuación, se muestra un resumen de diversas convenciones de la documentación de ADO, codificadas en Visual Basic, así como sus equivalentes en Visual C++.

### <a name="declaring-an-ado-object"></a>Declaración de un objeto ADO

En Visual Basic, una variable de objeto ADO (en este caso, de un objeto **Recordset**) se declara del siguiente modo:

```vb 
 
Dim rst As ADODB.Recordset 
```

La cláusula, "ADODB. Recordset", es el ProgID del **objeto Recordset** tal como se define en el Registro. Una instancia nueva de un objeto **Record** se declara del siguiente modo:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-o-

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

En Visual C++, la **\# directiva import** genera declaraciones de tipo puntero inteligentes para todos los objetos ADO. Por ejemplo, una variable que apunta a un **\_ objeto Recordset** es de tipo **\_ RecordsetPtr** y se declara de la siguiente manera:

```cpp 
 
_RecordsetPtr rs; 
```

A variable that points to a new instance of a **\_ Recordset** object is declared as follows:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-o-

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-o-

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

Después de llamar al método **CreateInstance**, la variable se puede utilizar de la manera siguiente:

```cpp 
 
rs->Open(...); 
```

Observe que, en un caso, el operador "." se usa como si la variable fuera una instancia de una clase (rs. CreateInstance) y, en otro caso, el operador "- " se usa como si la variable fuera un puntero a una \> interfaz (rs- \> Open).

Una variable se puede usar de dos maneras porque el operador "- " está sobrecargado para permitir que una instancia de una clase se comporte como un puntero \> a una interfaz. Un miembro de clase privada de la variable de instancia contiene un puntero a la interfaz **\_ Recordset;** el operador "- " devuelve ese puntero y el puntero devuelto tiene acceso a los miembros del \> **\_ objeto Recordset.**

### <a name="coding-a-missing-parameter"></a>Codificar un parámetro que falta

#### <a name="string"></a>Cadena

Cuando necesite codificar en Visual Basic un operando **String** ausente, simplemente omita el operando. Deberá especificar el operando en Visual C++. Codificar **\_ un bstr \_ t** que tenga una cadena vacía como valor.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

Cuando necesite codificar en Visual Basic un operando **Variant** ausente, simplemente omita el operando. En Visual C++, deberá especificar todos los operandos. Codifica un parámetro **Variant** que falta con una **\_ variante \_ t** establecida en el valor especial, DISP \_ E \_ PARAMNOTFOUND y type, VT \_ ERROR. Como alternativa, especifique **vtMissing**, que es una constante predefinida equivalente suministrada por la **\# directiva de** importación.

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-o usar -

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Declaración de una variante

En Visual Basic, un tipo **Variant** se declara con la instrucción **Dim** del siguiente modo:

```vb 
 
Dim VariableName As Variant 
```

En Visual C++, declare una variable como tipo **\_ variant \_ t**. A continuación se muestran algunas declaraciones de variante **\_ \_ t** esquemáticas.

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

En el siguiente ejemplo de Visual C++ se muestra el uso de **un SafeArray** usado con **\_ una variante \_ t**.

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

3. El esquema identificado por la constante enumerada, **adSchemaColumns**, está asociado a cuatro columnas de restricción: TABLE \_ CATALOG, TABLE \_ SCHEMA, TABLE \_ NAME y COLUMN \_ NAME. Por lo tanto, se crea una matriz de valores **Variant** con cuatro elementos. A continuación, se especifica un valor de restricción que corresponde a la tercera columna, NOMBRE DE \_ TABLA. El objeto **Recordset** que se devuelve consta de varias columnas, entre las que se incluyen las columnas de restricción. Los valores de las columnas de restricción para cada fila devuelta deben ser los mismos que los valores de restricción correspondientes.

4. Aquéllos familiarizados con **SafeArrays** se pueden sorprender del hecho de que no se llame a **SafeArrayDestroy**() antes de la salida. De hecho, llamar a **SafeArrayDestroy**() provocará en este caso una excepción en tiempo de ejecución. El motivo es que el destructor de vtCriteria llamará **a VariantClear**() cuando la variante **\_ \_ t** se salga del ámbito, lo que liberará **safearray**. Llamar **a SafeArrayDestroy**, sin borrar manualmente la variante **\_ \_ t**, haría que el destructor intentara borrar un puntero **SafeArray** no válido. Si se hiciera la llamada a **SafeArrayDestroy**, el código presentaría el siguiente aspecto:
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Sin embargo, es mucho más sencillo permitir que la **\_ variante \_ t** administre **safearray**.


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

En este ejemplo de Visual C++ se muestra **la propiedad Get** / **Put** /* *PutRef***.*

> [!NOTE]
> Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.

1. En este ejemplo se usan dos formas de argumento de cadena que faltan: una constante explícita, **strMissing** y una cadena que el compilador usará para crear una **\_ bstr \_ t temporal** que existirá para el ámbito del método **Open.**

2. No es necesario convertir el operando de rs- \> PutRefActiveConnection(cn) en (IDispatch ) porque el tipo del operando ya \* es (IDispatch \* ).
    
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

### <a name="using-getitemx-and-itemx"></a>Uso de GetItem(x) y Item \[ x\]

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

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Conversión de punteros de objeto ADO con (IDispatch \* )

El siguiente ejemplo de Visual C++ muestra el uso de ( IDispatch \* ) para convertir explícitamente punteros a objetos ADO.

> [!NOTE]
> [!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.

1. Especifique un objeto **Connection** abierto en un **Variant** codificado explícitamente. Cast it with (IDispatch \* ) so the correct constructor will be invoked. Además, establezca explícitamente el segundo parámetro **\_ variant \_ t** en el valor predeterminado de **true,** por lo que el recuento de referencias de objeto será correcto cuando finalice la operación **Recordset::Open.**

2. La expresión , ( bstr t), no es una conversión, sino un operador variant t que extrae una cadena \_ \_ **\_ bstr \_ t** **\_ \_** de **variant** devuelta por **Value**. La expresión ( char ), no es una conversión, sino un operador bstr t que extrae un puntero a la cadena \* encapsulada en un **\_ objeto bstr \_ t.** **\_ \_** Esta sección de código muestra algunos de los comportamientos útiles de **\_ los operadores variant \_ t** y **\_ bstr \_ t.**
    
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

