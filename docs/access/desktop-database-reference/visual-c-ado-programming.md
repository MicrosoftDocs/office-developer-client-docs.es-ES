---
title: Programación de ADO en Visual C++
TOCTitle: Visual C++ ADO Programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21f832c227d706f8b12601e3346beb0c30ba0e78
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485268"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="00351-102">Programación de ADO en Visual C++</span><span class="sxs-lookup"><span data-stu-id="00351-102">Visual C++ ADO Programming</span></span>


<span data-ttu-id="00351-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00351-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00351-104">La Referencia de la API de ADO describe la funcionalidad de la interfaz de programación de aplicaciones (API) de ADO mediante una sintaxis similar a Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="00351-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="00351-105">Aunque los destinatarios son todos los usuarios, los programadores de ADO emplean diversos lenguajes como Visual Basic, Visual C++ (con y sin el \*\* \#importar\*\* directiva) y Visual J ++ (con el paquete de clases ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="00351-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="00351-106">Para dar cabida a esta diversidad, los [Índices de sintaxis de ADO para Visual C++](using-ado-with-microsoft-visual-c.md) proporcionan sintaxis específica de Visual C++ con vínculos a descripciones comunes de funcionalidad, parámetros, comportamientos excepcionales, etc., en la Referencia de la API.</span><span class="sxs-lookup"><span data-stu-id="00351-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="00351-p102">ADO se implementa con interfaces COM (Modelo de objetos componentes). Sin embargo, es más fácil para los programadores trabajar con COM en algunos lenguajes de programación que en otros. Por ejemplo, casi todos los detalles del uso de COM se manejan implícitamente en Visual Basic, mientras que en Visual C++ son los programadores quienes deben manejar esos detalles.</span><span class="sxs-lookup"><span data-stu-id="00351-p102">ADO is implemented with COM (Component Object Model) interfaces. However, it is easier for programmers to work with COM in certain programming languages than others. For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="00351-110">En las secciones siguientes resumen la información para los programadores de C y C++ que utilizan ADO y la \*\* \#importar\*\* directiva.</span><span class="sxs-lookup"><span data-stu-id="00351-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="00351-111">Se centra en tipos de datos específicos de COM (**Variant**, **BSTR**y **SafeArray**) y tratamiento de errores (\_com\_error).</span><span class="sxs-lookup"><span data-stu-id="00351-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="00351-112">Uso de la \#Importar directiva del compilador</span><span class="sxs-lookup"><span data-stu-id="00351-112">Using the \#import Compiler Directive</span></span>

<span data-ttu-id="00351-113">La \*\* \#importar\*\* directiva del compilador de Visual C++ simplifica el trabajo con las propiedades y métodos de ADO.</span><span class="sxs-lookup"><span data-stu-id="00351-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="00351-114">La directiva toma el nombre de un archivo que contiene una biblioteca de tipos, tal como la dll de ADO (Msado15.dll), y genera archivos de encabezado que contienen declaraciones typedef, punteros inteligentes para interface y constantes enumeradas.</span><span class="sxs-lookup"><span data-stu-id="00351-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="00351-115">Cada interfaz se encapsula o engloba en una clase.</span><span class="sxs-lookup"><span data-stu-id="00351-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="00351-p105">Para cada operación dentro de una clase (es decir una llamada a método o propiedad), existe una declaración para llamar a la operación directamente (es decir, la forma "original" de la operación) y una declaración para llamar a la operación original y generar un error COM si la operación no se ejecuta correctamente. Si la operación es una propiedad, suele existir una directiva del compilador que crea una sintaxis alternativa para la operación que tiene sintaxis similar a Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="00351-p105">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully. If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="00351-118">Las operaciones que recuperan el valor de una propiedad tienen nombres de la forma, \**obtener \*\*\* (propiedad)*.</span><span class="sxs-lookup"><span data-stu-id="00351-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="00351-119">Las operaciones que establezca el valor de una propiedad tienen nombres de la forma, \**colocar \*\*\* (propiedad)*.</span><span class="sxs-lookup"><span data-stu-id="00351-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="00351-120">Las operaciones que establecen el valor de una propiedad con un puntero a un objeto ADO tienen nombres de la forma, \**PutRef \*\*\* (propiedad)*.</span><span class="sxs-lookup"><span data-stu-id="00351-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="00351-121">Puede obtener o establecer una propiedad con llamadas de este tipo:</span><span class="sxs-lookup"><span data-stu-id="00351-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="00351-122">Utilizar directivas de propiedad</span><span class="sxs-lookup"><span data-stu-id="00351-122">Using Property Directives</span></span>

<span data-ttu-id="00351-123">La \*\* \_ \_declspec(property...)\*\* directiva del compilador es una extensión del lenguaje C específica de Microsoft que declara una función utilizada como una propiedad que tenga una sintaxis alternativa.</span><span class="sxs-lookup"><span data-stu-id="00351-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="00351-124">Como resultado, puede establecer u obtener valores de una propiedad de forma similar a Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="00351-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="00351-125">Por ejemplo, puede establecer y obtener una propiedad de este modo:</span><span class="sxs-lookup"><span data-stu-id="00351-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="00351-126">Tenga en cuenta que no tiene que escribir este código:</span><span class="sxs-lookup"><span data-stu-id="00351-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="00351-127">El compilador generará la adecuada \*\*Get \*\**-*, **Put**-, o \**PutRef \*\*\* (propiedad)* llamada según la sintaxis alternativa declarada y si la propiedad se va a leer o escribir.</span><span class="sxs-lookup"><span data-stu-id="00351-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="00351-128">La \*\* \_ \_declspec(property...)\*\* directiva del compilador sólo puede declarar **get**, **put**o **get** y **put** sintaxis alternativa para una función.</span><span class="sxs-lookup"><span data-stu-id="00351-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="00351-129">Las operaciones de solo lectura sólo tienen una declaración **get** ; operaciones de sólo escritura únicamente tienen una declaración **put** ; las operaciones que son de lectura y escritura tienen declaraciones **get** y **put** .</span><span class="sxs-lookup"><span data-stu-id="00351-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="00351-130">Sólo hay dos declaraciones son posibles con esta directiva; Sin embargo, cada propiedad tiene tres funciones: \**obtener \*\*\* (propiedad)*, \**colocar \*\*\* (propiedad)*, y \**PutRef \*\*\* (propiedad)*.</span><span class="sxs-lookup"><span data-stu-id="00351-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="00351-131">En ese caso, sólo dos formas de la propiedad presentan sintaxis alternativa.</span><span class="sxs-lookup"><span data-stu-id="00351-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="00351-132">Por ejemplo, la propiedad **ActiveConnection** del objeto **Command** se declara con una sintaxis alternativa para \**obtener \*\*\* ActiveConnection* y \**PutRef \*\*\* ActiveConnection*.</span><span class="sxs-lookup"><span data-stu-id="00351-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="00351-133">**PutRef**- sintaxis es una buena opción debido a que en la práctica, normalmente desean colocar un objeto **Connection** abierto (es decir, un puntero de objeto de **conexión** ) en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="00351-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="00351-134">Por otro lado, el objeto **Recordset** tiene **Get**-, **Put**-, y \**PutRef \*\*\* ActiveConnection* las operaciones, pero sin sintaxis alternativa.</span><span class="sxs-lookup"><span data-stu-id="00351-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="00351-135">Colecciones, el método GetItem y la propiedad Item</span><span class="sxs-lookup"><span data-stu-id="00351-135">Collections, the GetItem Method, and the Item Property</span></span>

<span data-ttu-id="00351-p111">ADO define varias colecciones, incluidas **Fields**, **Parameters**, **Properties** y **Errors**. En Visual C++, el método **GetItem(***índice***)** devuelve un miembro de la colección. *Índice* es de un tipo **Variant**, cuyo valor es el índice numérico del miembro de la colección o una cadena que contiene el nombre del miembro.</span><span class="sxs-lookup"><span data-stu-id="00351-p111">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**. In Visual C++, the **GetItem(***index***)** method returns a member of the collection. *Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="00351-139">La \*\* \_ \_declspec(property...)\*\* directiva del compilador declara la propiedad **Item** como una sintaxis alternativa al método **GetItem()** fundamental de cada colección.</span><span class="sxs-lookup"><span data-stu-id="00351-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="00351-140">La sintaxis alternativa utiliza corchetes y es similar a una referencia a matriz.</span><span class="sxs-lookup"><span data-stu-id="00351-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="00351-141">En general, las dos formas son similares a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00351-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="00351-142">Por ejemplo, asignar un valor a un campo de un objeto **Recordset** , denominado ***rs***, derivado de la tabla **authors** de la base de datos **pubs** .</span><span class="sxs-lookup"><span data-stu-id="00351-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="00351-143">Utilice la propiedad **Item()** para obtener acceso al tercer **campo** de la colección **Fields** del objeto **Recordset** (las colecciones se indizan desde cero; suponga que el tercer campo se denomina ***au\_fname***).</span><span class="sxs-lookup"><span data-stu-id="00351-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="00351-144">A continuación, llame al método **Value()** sobre el objeto **Field** para asignar un valor de tipo string.</span><span class="sxs-lookup"><span data-stu-id="00351-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="00351-145">Esto se puede expresar en Visual Basic de las siguientes cuatro maneras (las últimas dos formas son exclusivas de Visual Basic; otros lenguajes no tienen equivalentes):</span><span class="sxs-lookup"><span data-stu-id="00351-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="00351-146">El equivalente en Visual C++ a las dos primeras formas anteriores es:</span><span class="sxs-lookup"><span data-stu-id="00351-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="00351-147">\-o -(también se muestra la sintaxis alternativa de la propiedad **Value** )</span><span class="sxs-lookup"><span data-stu-id="00351-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="00351-148">Tipos de datos específicos de COM</span><span class="sxs-lookup"><span data-stu-id="00351-148">COM-Specific Data Types</span></span>

<span data-ttu-id="00351-p114">En general, cualquier tipo de datos de Visual Basic que se encuentra en la Referencia de la API de ADO tiene un equivalente en Visual C++. Éstos incluyen tipos de datos estándar, tales como **unsigned char** para un **Byte** de Visual Basic, **short** para **Integer** y **long** para **Long**. Busque en los Índices de la sintaxis para ver qué se requiere exactamente para los operandos de un método o una propiedad dados.</span><span class="sxs-lookup"><span data-stu-id="00351-p114">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent. These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**. Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="00351-152">Las excepciones a esta regla son los tipo de datos específicos de COM: **Variant**, **BSTR** y **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="00351-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

## <a name="variant"></a><span data-ttu-id="00351-153">Variant</span><span class="sxs-lookup"><span data-stu-id="00351-153">Variant</span></span>

<span data-ttu-id="00351-p115">Un **Variant** es un tipo de datos estructurados que contiene un miembro de valor y un miembro de tipo de datos. Un **Variant** puede contener una amplia variedad de otros tipos de datos, incluidos otro Variant, BSTR, Boolean, IDispatch, puntero a IUnknown, moneda, fecha, etc. COM también proporciona métodos que facilitan la conversión de un tipo de datos en otro.</span><span class="sxs-lookup"><span data-stu-id="00351-p115">A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="00351-157">La \*\* \_variant\_t\*\* clase encapsula y administra el tipo de datos **Variant** .</span><span class="sxs-lookup"><span data-stu-id="00351-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="00351-158">Cuando la referencia de API de ADO indica que un método u operando propiedad toma un valor, suele significar que el valor se pasa en un \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="00351-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="00351-p116">Esta regla se cumple explícitamente cuando la sección **Parámetros** de los temas de la Referencia de la API de ADO indica que un operando es de tipo **Variant**. Una excepción es cuando la documentación indica explícitamente que el operandos toma un tipo de datos estándar, como **Long**, **Byte** o una enumeración. Otra excepción es cuando el operando toma un **String**.</span><span class="sxs-lookup"><span data-stu-id="00351-p116">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.</span></span>

## <a name="bstr"></a><span data-ttu-id="00351-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="00351-162">BSTR</span></span>

<span data-ttu-id="00351-p117">Un **BSTR** (**B**asic **STR**ing) es un tipo de datos estructurados que contiene una cadena de caracteres y la longitud de la cadena. COM proporciona métodos para asignar, manipular y liberar un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="00351-p117">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length. COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="00351-165">La \*\* \_bstr\_t\*\* clase encapsula y administra el tipo de datos **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="00351-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="00351-166">Cuando la referencia de API de ADO indica que un método o una propiedad toman un valor de **tipo String** , significa que el valor se encuentra en el formulario de un \*\* \_bstr\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="00351-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

## <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="00351-167">Convirtiendo \_variant\_t y \_bstr\_clases t</span><span class="sxs-lookup"><span data-stu-id="00351-167">Casting \_variant\_t and \_bstr\_t Classes</span></span>

<span data-ttu-id="00351-168">A menudo no es necesario para el código de forma explícita una \*\* \_variant\_t\*\* o \*\* \_bstr\_t\*\* en un argumento para una operación.</span><span class="sxs-lookup"><span data-stu-id="00351-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="00351-169">Si el \*\* \_variant\_t\*\* o \*\* \_bstr\_t\*\* clase tiene un constructor que coincide con el tipo de datos del argumento, a continuación, el compilador generará la adecuada \*\* \_variant\_t\*\* o \*\* \_ BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="00351-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="00351-170">Sin embargo, si el argumento es ambiguo, es decir, el tipo de datos del argumento coincide con más de un constructor, deberá convertir el argumento explícitamente al tipo de datos apropiado para llamar al constructor correcto.</span><span class="sxs-lookup"><span data-stu-id="00351-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="00351-171">Por ejemplo, la declaración para el método **Recordset::Open** es:</span><span class="sxs-lookup"><span data-stu-id="00351-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="00351-172">El argumento ActiveConnection acepta una referencia a un \*\* \_variant\_t\*\*, que se puede codificar como una cadena de conexión o un puntero a un objeto **Connection** abierto.</span><span class="sxs-lookup"><span data-stu-id="00351-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="00351-173">La correcta \*\* \_variant\_t\*\* se construirá implícitamente si se pasa una cadena tal como "DSN = pubs; uid = sa; pwd =;", o un puntero tal como "(IDispatch \*) pConn".</span><span class="sxs-lookup"><span data-stu-id="00351-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="00351-174">O bien, puede codificar explícitamente un \*\* \_variant\_t\*\* que contiene un puntero tal como "\_variant\_t ((IDispatch \*) pConn, true)".</span><span class="sxs-lookup"><span data-stu-id="00351-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="00351-175">La conversión explícita, (IDispatch \*), resuelve la ambigüedad con otro constructor que toma un puntero a una interfaz IUnknown.</span><span class="sxs-lookup"><span data-stu-id="00351-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="00351-p120">Es un hecho crucial (aunque raramente mencionado) que ADO es una interfaz IDispatch. Siempre que un puntero a un objeto ADO se deba pasar como un **Variant**, es necesario convertir explícitamente ese puntero a un puntero a un interfaz IDispatch.</span><span class="sxs-lookup"><span data-stu-id="00351-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="00351-178">El último caso codifica explícitamente el segundo argumento booleano del constructor con su valor predeterminado opcional true.</span><span class="sxs-lookup"><span data-stu-id="00351-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="00351-179">Este argumento hace que el constructor de **tipo Variant** llamar al método **AddRef**(), que compensa a ADO automáticamente llamando el \*\* \_variant\_t::Release\*\*(método) () una vez completada la llamada al método o propiedad de ADO.</span><span class="sxs-lookup"><span data-stu-id="00351-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

## <a name="safearray"></a><span data-ttu-id="00351-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="00351-180">SafeArray</span></span>

<span data-ttu-id="00351-181">Un **SafeArray** es un tipo de datos estructurados que contiene una matriz de otros tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="00351-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="00351-182">Un **SafeArray** se denomina *seguros* porque contiene información acerca de los límites de cada dimensión de la matriz y limita el acceso a elementos de la matriz a esos límites.</span><span class="sxs-lookup"><span data-stu-id="00351-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="00351-183">Cuando la Referencia de la API de ADO indica que un método o una propiedad acepta o devuelve una matriz, significa que el método o la propiedad acepta o devuelve un **SafeArray** no una matriz nativa de C/C++.</span><span class="sxs-lookup"><span data-stu-id="00351-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="00351-p123">Por ejemplo, el segundo parámetro del método **OpenSchema** del objeto **Conection** requiere una matriz de valores **Variant**. Esos valores **Variant** se deben pasar como elementos de un **SafeArray**, y ese **SafeArray** se debe establecer como el valor de otro **Variant**. Es ese otro **Variant** el que se pasa como el segundo argumento de **OpenSchema**.</span><span class="sxs-lookup"><span data-stu-id="00351-p123">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values. Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**. It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="00351-187">Como ejemplos adicionales, el primer argumento del método **Find** es un **Variant** cuyo valor es un **SafeArray** unidimensional, cada uno de los argumentos primero y segundo opcionales de **AddNew** es un **SafeArray** unidimensional y el valor devuelto del método **GetRows** es un **Variant** cuyo valor es un **SafeArray** bidimensional.</span><span class="sxs-lookup"><span data-stu-id="00351-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="00351-188">Parámetros predeterminados y ausentes</span><span class="sxs-lookup"><span data-stu-id="00351-188">Missing and Default Parameters</span></span>

<span data-ttu-id="00351-p124">Visual Basic permite que falten parámetros en los métodos. Por ejemplo, el método **Open** de un objeto **Recordset** tiene cinco parámetros, pero se pueden omitir parámetros intermedios y no incluir parámetros finales. Se usará entonces un **BSTR** o **Variant** predeterminado según el tipo de datos del operando que falte.</span><span class="sxs-lookup"><span data-stu-id="00351-p124">Visual Basic allows missing parameters in methods. For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters. A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="00351-192">En C/C++, se deben especificar todos los operandos.</span><span class="sxs-lookup"><span data-stu-id="00351-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="00351-193">Si desea especificar un parámetro que falta cuyo tipo de datos es una cadena, especifique un \*\* \_bstr\_t\*\* que contenga una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="00351-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="00351-194">Si desea especificar un parámetro que falta cuyo tipo de datos es un **tipo Variant**, especifique un \*\* \_variant\_t\*\* con un valor de DISP\_E\_PARAMNOTFOUND y un tipo de VT\_ERROR.</span><span class="sxs-lookup"><span data-stu-id="00351-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="00351-195">Como alternativa, especifique el equivalente \*\* \_variant\_t\*\* constante, **vtMissing**, que es proporcionado por el \*\* \#importar\*\* directiva.</span><span class="sxs-lookup"><span data-stu-id="00351-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="00351-p126">Existen tres métodos que constituyen excepciones al uso típico de **vtMissing**. Éstos son los métodos **Execute** de los objetos **Connection** y **Command**, y el método **NextRecordset** del objeto **Recordset**. Las siguientes son sus firmas:</span><span class="sxs-lookup"><span data-stu-id="00351-p126">Three methods are exceptions to the typical use of **vtMissing**. These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object. The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="00351-p127">Los parámetros *RecordsAffected* y *Parameters*son punteros a un **Variant**. *Parameters* es un parámetro de entrada que especifica la dirección de un **Variant** que contiene un parámetro único, o una matriz de parámetros, que modificará el comando que se va a ejecutar. *RecordsAffected* es un parámetro de salida que especifica la dirección de un **Variant** donde se devuelve el número de filas afectadas por el método.</span><span class="sxs-lookup"><span data-stu-id="00351-p127">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**. *Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed. *RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="00351-202">En el método **Execute** del **comando** objeto, indique que se ha especificado ningún parámetro estableciendo *parámetros* en cualquiera \&vtMissing (que se recomienda) o como el puntero nulo (es decir, **NULL** o cero (0)).</span><span class="sxs-lookup"><span data-stu-id="00351-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="00351-203">Si *los parámetros* se establece como el puntero nulo, el método sustituye internamente el equivalente de **vtMissing**y, a continuación, completa la operación.</span><span class="sxs-lookup"><span data-stu-id="00351-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="00351-204">En todos los métodos, indique que no se debe devolver el número de registros afectados estableciendo *RecordsAffected* como el puntero nulo.</span><span class="sxs-lookup"><span data-stu-id="00351-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="00351-205">En este caso, el puntero nulo no es tanto un parámetro que falta como una indicación de que el método debería descartar el número de registros afectados.</span><span class="sxs-lookup"><span data-stu-id="00351-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="00351-206">Por tanto, para estos tres métodos, es correcto codificar del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="00351-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="00351-207">Tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="00351-207">Error Handling</span></span>

<span data-ttu-id="00351-208">En COM, la mayoría de las operaciones devolverá un código de retorno HRESULT que indica si una función se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="00351-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="00351-209">La \*\* \#importar\*\* directiva genera código contenedor alrededor de cada método "sin procesar" o la propiedad y comprueba el HRESULT devuelto.</span><span class="sxs-lookup"><span data-stu-id="00351-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="00351-210">Si el HRESULT indica error, el código de contenedor genera un error COM llamando a \_com\_problema\_errorex() con el HRESULT devolver código como un argumento.</span><span class="sxs-lookup"><span data-stu-id="00351-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="00351-211">Objetos de error COM se pueden capturar en **probar**-bloque**catch** .</span><span class="sxs-lookup"><span data-stu-id="00351-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="00351-212">(Para una mayor eficacia, detecte una referencia a un \*\* \_com\_error\*\* objeto.)</span><span class="sxs-lookup"><span data-stu-id="00351-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="00351-p131">Recuerde que éstos son errores de ADO (resultado de una operación ADO). Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="00351-p131">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="00351-215">La \*\* \#importar\*\* directiva sólo crea errores rutinas de tratamiento de los métodos y propiedades declaradas en la DLL de ADO.</span><span class="sxs-lookup"><span data-stu-id="00351-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="00351-216">Sin embargo, puede aprovechar este mismo mecanismo de tratamiento de errores escribiendo su propia función en línea o macro de comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="00351-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="00351-217">Vea el tema [Extensiones de Visual C++](visual-c-extensions-for-ado.md) o el código de la sección siguiente para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="00351-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="00351-218">Equivalentes en Visual C++ de las convenciones de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="00351-218">Visual C++ Equivalents of Visual Basic Conventions</span></span>

<span data-ttu-id="00351-219">A continuación, se muestra un resumen de diversas convenciones de la documentación de ADO, codificadas en Visual Basic, así como sus equivalentes en Visual C++.</span><span class="sxs-lookup"><span data-stu-id="00351-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

## <a name="declaring-an-ado-object"></a><span data-ttu-id="00351-220">Declaración de un objeto ADO</span><span class="sxs-lookup"><span data-stu-id="00351-220">Declaring an ADO Object</span></span>

<span data-ttu-id="00351-221">En Visual Basic, una variable de objeto ADO (en este caso, de un objeto **Recordset** ) se declara del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="00351-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="00351-222">La cláusula "ADODB. Objeto Recordset"es el ProgID del objeto **Recordset** tal como se define en el registro.</span><span class="sxs-lookup"><span data-stu-id="00351-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="00351-223">Una instancia nueva de un objeto **Record** se declara del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="00351-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="00351-224">\-o -</span><span class="sxs-lookup"><span data-stu-id="00351-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="00351-225">En Visual C++, la \*\* \#importar\*\* directiva genera declaraciones de tipo puntero inteligente para todos los objetos de ADO.</span><span class="sxs-lookup"><span data-stu-id="00351-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="00351-226">Por ejemplo, una variable que apunta a un \*\* \_Recordset\*\* objeto es del tipo \*\* \_RecordsetPtr\*\*y se declara del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="00351-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="00351-227">Una variable que apunta a una nueva instancia de un \*\* \_Recordset\*\* objeto se declara del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="00351-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="00351-228">\-o -</span><span class="sxs-lookup"><span data-stu-id="00351-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="00351-229">\-o -</span><span class="sxs-lookup"><span data-stu-id="00351-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="00351-230">Después de llamar al método **CreateInstance**, la variable se puede utilizar de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="00351-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="00351-231">Tenga en cuenta que en un caso, el "." se usa el operador como si la variable fuera una instancia de una clase (rs. CreateInstance) y en otro caso, el "-\>" se usa el operador como si la variable fuera un puntero a una interfaz (rs -\>Open).</span><span class="sxs-lookup"><span data-stu-id="00351-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="00351-232">Una variable se puede utilizar de dos maneras debido a que la "-\>" operador está sobrecargado para permitir que una instancia de una clase que se comporte como un puntero a una interfaz.</span><span class="sxs-lookup"><span data-stu-id="00351-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="00351-233">Un miembro privado de clase de la variable de instancia contiene un puntero a la \*\* \_Recordset\*\* de la interfaz; la "-\>" operador devuelve ese puntero; y el puntero devuelto obtiene acceso a los miembros de la \*\* \_Recordset\*\* objeto.</span><span class="sxs-lookup"><span data-stu-id="00351-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

## <a name="coding-a-missing-parameter"></a><span data-ttu-id="00351-234">Codificar un parámetro que falta:</span><span class="sxs-lookup"><span data-stu-id="00351-234">Coding a Missing Parameter</span></span>

<span data-ttu-id="00351-235">Cuando necesite codificar en Visual Basic un operando **String** ausente, simplemente omita el operando.</span><span class="sxs-lookup"><span data-stu-id="00351-235">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="00351-236">Deberá especificar el operando en Visual C++.</span><span class="sxs-lookup"><span data-stu-id="00351-236">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="00351-237">Código un \*\* \_bstr\_t\*\* que tiene una cadena vacía como un valor.</span><span class="sxs-lookup"><span data-stu-id="00351-237">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

## <a name="coding-a-missing-parameter"></a><span data-ttu-id="00351-238">Codificar un parámetro que falta:</span><span class="sxs-lookup"><span data-stu-id="00351-238">Coding a Missing Parameter</span></span>

<span data-ttu-id="00351-239">Cuando necesite codificar en Visual Basic un operando **Variant** ausente, simplemente omita el operando.</span><span class="sxs-lookup"><span data-stu-id="00351-239">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="00351-240">En Visual C++, deberá especificar todos los operandos.</span><span class="sxs-lookup"><span data-stu-id="00351-240">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="00351-241">Codifique un parámetro **Variant** ausente con un \*\* \_variant\_t\*\* establecida en el valor especial, DISP\_E\_PARAMNOTFOUND y tipo, VT\_ERROR.</span><span class="sxs-lookup"><span data-stu-id="00351-241">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="00351-242">Como alternativa, especifique **vtMissing**, que es equivalente a un constante predefinido proporcionados por la \*\* \#importar\*\* directiva.</span><span class="sxs-lookup"><span data-stu-id="00351-242">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="00351-243">\-o utilice-</span><span class="sxs-lookup"><span data-stu-id="00351-243">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

## <a name="declaring-a-variant"></a><span data-ttu-id="00351-244">Declaración de un Variant</span><span class="sxs-lookup"><span data-stu-id="00351-244">Declaring a Variant</span></span>

<span data-ttu-id="00351-245">En Visual Basic, un tipo **Variant** se declara con la instrucción **Dim** del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="00351-245">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="00351-246">En Visual C++, declare una variable como tipo de \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="00351-246">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="00351-247">Esquema unos \*\* \_variant\_t\*\* declaraciones se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="00351-247">A few schematic **\_variant\_t** declarations are shown below.</span></span>


> [!NOTE]
> <P><span data-ttu-id="00351-p139">[!NOTA] Estas declaraciones simplemente proporcionan una idea general de cómo podría codificar su propio programa. Para obtener más información, vea los ejemplos siguientes y la documentación de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="00351-p139">These declarations merely give a rough idea of what you would code in your own program. For more information, see the examples below, and the Visual C++ documentation.</span></span></P>



```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

## <a name="using-arrays-of-variants"></a><span data-ttu-id="00351-250">Utilizar matrices de Variants</span><span class="sxs-lookup"><span data-stu-id="00351-250">Using Arrays of Variants</span></span>

<span data-ttu-id="00351-251">En Visual Basic, las matrices de **Variants** se pueden codificar con la instrucción **Dim** o utilizar la función **Array**, tal como se muestra en el código de ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00351-251">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

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

<span data-ttu-id="00351-252">El siguiente ejemplo de Visual C++ muestra cómo utilizar un **SafeArray** con un \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="00351-252">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="00351-253">[!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="00351-253">The following notes correspond to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="00351-254">Una vez más, se define la función inline TESTHR() para aprovechar el mecanismo de control de errores existente.</span><span class="sxs-lookup"><span data-stu-id="00351-254">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2.  <span data-ttu-id="00351-p140">Sólo necesitará una matriz unidimensional, de forma que pueda utilizar **SafeArrayCreateVector** en lugar de la declaración de propósito general **SAFEARRAYBOUND** y la función **SafeArrayCreate**. El código que utiliza **SafeArrayCreate** tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="00351-p140">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function. The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
    ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
    ```

3.  <span data-ttu-id="00351-257">El esquema identificado por la constante enumerada **adSchemaColumns**se asocia con cuatro columnas de restricción: tabla\_catálogo, tabla\_esquema, tabla\_nombre y columna\_nombre.</span><span class="sxs-lookup"><span data-stu-id="00351-257">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="00351-258">Por lo tanto, se crea una matriz de valores **Variant** con cuatro elementos.</span><span class="sxs-lookup"><span data-stu-id="00351-258">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="00351-259">A continuación, un valor de restricción que corresponde a la tercera columna, tabla\_nombre, se ha especificado.</span><span class="sxs-lookup"><span data-stu-id="00351-259">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="00351-260">El objeto **Recordset** que se devuelve consta de varias columnas, entre las que se incluyen las columnas de restricción.</span><span class="sxs-lookup"><span data-stu-id="00351-260">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="00351-261">Los valores de las columnas de restricción para cada fila devuelta deben ser los mismos que los valores de restricción correspondientes.</span><span class="sxs-lookup"><span data-stu-id="00351-261">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4.  <span data-ttu-id="00351-262">Aquellos que estén familiarizados con **SAFEARRAY** se sorprendan que no se llama a **SafeArrayDestroy**() antes de la salida.</span><span class="sxs-lookup"><span data-stu-id="00351-262">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="00351-263">De hecho, llamar a **SafeArrayDestroy**() provocará en este caso una excepción de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="00351-263">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="00351-264">La razón es que el destructor de vtCriteria llamará a () **VariantClear**cuando la \*\* \_variant\_t\*\* queda fuera del ámbito, lo que liberará el **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="00351-264">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="00351-265">La llamada a **SafeArrayDestroy**, sin borrar manualmente el \*\* \_variant\_t\*\*, hará que el destructor intente borrar un puntero **SafeArray** no válido.</span><span class="sxs-lookup"><span data-stu-id="00351-265">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="00351-266">Si se hiciera la llamada a **SafeArrayDestroy**, el código presentaría el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="00351-266">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
    ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
    ```
    
    <span data-ttu-id="00351-267">Sin embargo, resulta más sencillo permitir que el \*\* \_variant\_t\*\* administre el **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="00351-267">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>

<!-- end list -->

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

## <a name="using-property-getputputref"></a><span data-ttu-id="00351-268">Utilizar Get/Put/PutRef Propiedad</span><span class="sxs-lookup"><span data-stu-id="00351-268">Using Property Get/Put/PutRef</span></span>

<span data-ttu-id="00351-269">En Visual Basic, el nombre de una propiedad no indica si ésta se ha recuperado, si se le ha asignado un valor o se le ha asignado una referencia.</span><span class="sxs-lookup"><span data-stu-id="00351-269">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

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

<span data-ttu-id="00351-270">En este ejemplo de Visual C++ muestra cómo **obtener**/**colocar**/\**PutRef \*\*\* (propiedad)*.</span><span class="sxs-lookup"><span data-stu-id="00351-270">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>


> [!NOTE]
> <P><span data-ttu-id="00351-271">[!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="00351-271">The following notes correspond to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="00351-272">En este ejemplo se utiliza dos formas de un argumento de cadena que falta: una constante explícita, **strMissing**y una cadena que el compilador utilizará para crear un archivo temporal \*\* \_bstr\_t\*\* que existirá durante el ámbito del método **Open** .</span><span class="sxs-lookup"><span data-stu-id="00351-272">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2.  <span data-ttu-id="00351-273">No es necesario convertir explícitamente el operando de rs -\>PutRefActiveConnection a (IDispatch \*) porque el tipo del operando es ya (IDispatch \*).</span><span class="sxs-lookup"><span data-stu-id="00351-273">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
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

## <a name="using-getitemx-and-itemx"></a><span data-ttu-id="00351-274">Utilizar GetItem y elemento\[x\]</span><span class="sxs-lookup"><span data-stu-id="00351-274">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="00351-275">Este ejemplo de Visual Basic muestra la sintaxis estándar y alternativa para **Item**().</span><span class="sxs-lookup"><span data-stu-id="00351-275">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

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

<span data-ttu-id="00351-276">En este ejemplo de Visual C++, se muestra el uso de **Item**.</span><span class="sxs-lookup"><span data-stu-id="00351-276">This Visual C++ example demonstrates **Item**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="00351-277">[!NOTA] La nota siguiente corresponde a secciones comentadas en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="00351-277">The following note corresponds to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="00351-278">Cuando se obtiene acceso a la colección mediante **Item**, el índice, **2**, se debe convertir explícitamente a **long** para que se realice la llamada al constructor apropiado.</span><span class="sxs-lookup"><span data-stu-id="00351-278">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
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

## <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="00351-279">Convertir explícitamente punteros a objetos ADO con ( IDispatch \* )</span><span class="sxs-lookup"><span data-stu-id="00351-279">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="00351-280">El siguiente ejemplo de Visual C++ muestra el uso de ( IDispatch \* ) para convertir explícitamente punteros a objetos ADO.</span><span class="sxs-lookup"><span data-stu-id="00351-280">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>


> [!NOTE]
> <P><span data-ttu-id="00351-281">[!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="00351-281">The following notes correspond to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="00351-282">Especifique un objeto **Connection** abierto en un **Variant** codificado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="00351-282">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="00351-283">Conviértalo explícitamente con (IDispatch \*) por lo que se invocará el constructor correcto.</span><span class="sxs-lookup"><span data-stu-id="00351-283">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="00351-284">Además, establezca explícitamente el segundo \*\* \_variant\_t\*\* parámetro para el valor predeterminado **es true**, por lo que el recuento de referencia de objeto será correcto cuando termina la operación **Recordset:: Open** .</span><span class="sxs-lookup"><span data-stu-id="00351-284">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2.  <span data-ttu-id="00351-285">La expresión (\_bstr\_t), no es una conversión de tipos, pero un \*\* \_variant\_t\*\* operador que extrae una \*\* \_bstr\_t\*\* cadena del **tipo Variant** devuelto por **valor**.</span><span class="sxs-lookup"><span data-stu-id="00351-285">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="00351-286">La expresión (char\*), no es una conversión de tipos, pero un \*\* \_bstr\_t\*\* operador que extrae un puntero a la cadena encapsulado en un \*\* \_bstr\_t\*\* objeto.</span><span class="sxs-lookup"><span data-stu-id="00351-286">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="00351-287">En esta sección de código, se muestra algunos de los comportamientos útiles de \*\* \_variant\_t\*\* y \*\* \_bstr\_t\*\* operadores.</span><span class="sxs-lookup"><span data-stu-id="00351-287">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
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

