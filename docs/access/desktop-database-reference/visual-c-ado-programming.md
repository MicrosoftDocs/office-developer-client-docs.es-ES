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
# <a name="visual-c-ado-programming"></a><span data-ttu-id="b9915-102">Programación de ADO con Visual C++</span><span class="sxs-lookup"><span data-stu-id="b9915-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="b9915-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9915-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9915-104">La Referencia de la API de ADO describe la funcionalidad de la interfaz de programación de aplicaciones (API) de ADO mediante una sintaxis similar a Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b9915-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="b9915-105">Aunque la audiencia prevista es de todos los usuarios, los programadores de ADO emplean varios idiomas, como Visual Basic, Visual C++ (con y sin la directiva **\# de** importación) y Visual J++ (con el paquete de clase ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="b9915-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="b9915-106">Para dar cabida a esta diversidad, los [Índices de sintaxis de ADO para Visual C++](using-ado-with-microsoft-visual-c.md) proporcionan sintaxis específica de Visual C++ con vínculos a descripciones comunes de funcionalidad, parámetros, comportamientos excepcionales, etc., en la Referencia de la API.</span><span class="sxs-lookup"><span data-stu-id="b9915-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="b9915-p102">ADO se implementa con interfaces COM (Modelo de objetos componentes). Sin embargo, es más fácil para los programadores trabajar con COM en algunos lenguajes de programación que en otros. Por ejemplo, casi todos los detalles del uso de COM se manejan implícitamente en Visual Basic, mientras que en Visual C++ son los programadores quienes deben manejar esos detalles.</span><span class="sxs-lookup"><span data-stu-id="b9915-p102">ADO is implemented with COM (Component Object Model) interfaces. However, it is easier for programmers to work with COM in certain programming languages than others. For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="b9915-110">En las secciones siguientes se resumen los detalles para programadores de C y C++ mediante ADO y la **\# directiva de** importación.</span><span class="sxs-lookup"><span data-stu-id="b9915-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="b9915-111">Se centra en tipos de datos específicos de COM (**Variant**, **BSTR** y **SafeArray**) y control de errores ( \_ error \_ com).</span><span class="sxs-lookup"><span data-stu-id="b9915-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="b9915-112">Uso de \# la directiva del compilador de importación</span><span class="sxs-lookup"><span data-stu-id="b9915-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="b9915-113">La **\# directiva del** compilador de Importación de Visual C++ simplifica el trabajo con los métodos y propiedades de ADO.</span><span class="sxs-lookup"><span data-stu-id="b9915-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="b9915-114">La directiva toma el nombre de un archivo que contiene una biblioteca de tipos, tal como la dll de ADO (Msado15.dll), y genera archivos de encabezado que contienen declaraciones typedef, punteros inteligentes para interface y constantes enumeradas.</span><span class="sxs-lookup"><span data-stu-id="b9915-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="b9915-115">Cada interfaz se encapsula o engloba en una clase.</span><span class="sxs-lookup"><span data-stu-id="b9915-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="b9915-p105">Para cada operación dentro de una clase (es decir una llamada a método o propiedad), existe una declaración para llamar a la operación directamente (es decir, la forma "original" de la operación) y una declaración para llamar a la operación original y generar un error COM si la operación no se ejecuta correctamente. Si la operación es una propiedad, suele existir una directiva del compilador que crea una sintaxis alternativa para la operación que tiene sintaxis similar a Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b9915-p105">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully. If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="b9915-118">Las operaciones que recuperan el valor de una propiedad tienen nombres del formulario, \**Get\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="b9915-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="b9915-119">Las operaciones que establecen el valor de una propiedad tienen nombres del formulario, \**Put\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="b9915-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="b9915-120">Las operaciones que establecen el valor de una propiedad con un puntero a un objeto ADO tienen nombres del formulario, \**PutRef\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="b9915-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="b9915-121">Puede obtener o establecer una propiedad con llamadas de este tipo:</span><span class="sxs-lookup"><span data-stu-id="b9915-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="b9915-122">Uso de directivas de propiedades</span><span class="sxs-lookup"><span data-stu-id="b9915-122">Using property directives</span></span>

<span data-ttu-id="b9915-123">La directiva del compilador **\_ \_ declspec(property...)** es una extensión de lenguaje C específica de Microsoft que declara una función usada como propiedad para tener una sintaxis alternativa.</span><span class="sxs-lookup"><span data-stu-id="b9915-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="b9915-124">Como resultado, puede establecer u obtener valores de una propiedad de forma similar a Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b9915-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="b9915-125">Por ejemplo, puede establecer y obtener una propiedad de este modo:</span><span class="sxs-lookup"><span data-stu-id="b9915-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="b9915-126">Tenga en cuenta que no tiene que escribir este código:</span><span class="sxs-lookup"><span data-stu-id="b9915-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="b9915-127">El compilador generará la llamada adecuada \**Get\*\*\*-*, **Put**-, o \**PutRef\*\*\*Property* en función de la sintaxis alternativa que se declara y de si la propiedad se lee o escribe.</span><span class="sxs-lookup"><span data-stu-id="b9915-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="b9915-128">La **\_ \_ directiva del compilador declspec(property...)** solo  puede declarar **obtener,** **poner** o obtener y poner una **sintaxis** alternativa para una función.</span><span class="sxs-lookup"><span data-stu-id="b9915-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="b9915-129">Las operaciones de sólo lectura únicamente tienen una declaración **get**; las operaciones de sólo escritura únicamente tienen una declaración **put**; las operaciones de lectura y escritura tienen ambas declaraciones **get** y **put**.</span><span class="sxs-lookup"><span data-stu-id="b9915-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="b9915-130">Solo son posibles dos declaraciones con esta directiva; sin embargo, cada propiedad puede tener tres funciones de propiedad: \**Get\*\*\*Property*, \**Put\*\*\*Property* y \**PutRef\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="b9915-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="b9915-131">En ese caso, sólo dos formas de la propiedad presentan sintaxis alternativa.</span><span class="sxs-lookup"><span data-stu-id="b9915-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="b9915-132">Por ejemplo, la **propiedad Command** del objeto **ActiveConnection** se declara con una sintaxis alternativa para \**Get\*\*\*ActiveConnection* y \**PutRef\*\*\*ActiveConnection*.</span><span class="sxs-lookup"><span data-stu-id="b9915-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="b9915-133">La sintaxis de **PutRef** constituye una buena elección, ya que, en la práctica, deseará establecer un objeto **Connection** abierto (es decir, un puntero a un objeto **Connection**) en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b9915-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="b9915-134">Por otro lado, el **objeto Recordset** tiene operaciones **Get**-, **Put**-, y \**PutRef\*\*\*ActiveConnection,* pero sin sintaxis alternativa.</span><span class="sxs-lookup"><span data-stu-id="b9915-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="b9915-135">Colecciones, el método GetItem y la propiedad Item</span><span class="sxs-lookup"><span data-stu-id="b9915-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="b9915-136">ADO define varias colecciones, incluidas **Fields**, **Parameters**, **Properties** y **Errors**.</span><span class="sxs-lookup"><span data-stu-id="b9915-136">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**.</span></span> <span data-ttu-id="b9915-137">En Visual C++, el **método GetItem(***index***)** devuelve un miembro de la colección.</span><span class="sxs-lookup"><span data-stu-id="b9915-137">In Visual C++, the **GetItem(***index***)** method returns a member of the collection.</span></span> <span data-ttu-id="b9915-138">*Índice* es de un tipo **Variant**, cuyo valor es el índice numérico del miembro de la colección o una cadena que contiene el nombre del miembro.</span><span class="sxs-lookup"><span data-stu-id="b9915-138">*Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="b9915-139">La directiva del compilador **\_ \_ declspec(property...)** declara la **propiedad Item** como una sintaxis alternativa al método **getitem()** fundamental de cada colección.</span><span class="sxs-lookup"><span data-stu-id="b9915-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="b9915-140">La sintaxis alternativa utiliza corchetes y es similar a una referencia a matriz.</span><span class="sxs-lookup"><span data-stu-id="b9915-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="b9915-141">En general, las dos formas son similares a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b9915-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="b9915-142">Por ejemplo, asigne un valor a un campo de un objeto **Recordset**, denominado ***rs***, derivado de la tabla **authors** de la base de datos **pubs**.</span><span class="sxs-lookup"><span data-stu-id="b9915-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="b9915-143">Utilice la **propiedad Item()** para obtener acceso al tercer **campo** de la colección **Fields** del objeto **Recordset** (las colecciones se indizan desde cero; suponga que el tercer campo se denomina ***au \_ fname***).</span><span class="sxs-lookup"><span data-stu-id="b9915-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="b9915-144">A continuación, llame al método **Value()** sobre el objeto **Field** para asignar un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="b9915-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="b9915-145">Esto se puede expresar en Visual Basic de las siguientes cuatro maneras (las últimas dos formas son exclusivas de Visual Basic; otros lenguajes no tienen equivalentes):</span><span class="sxs-lookup"><span data-stu-id="b9915-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="b9915-146">El equivalente en Visual C++ a las dos primeras formas anteriores es:</span><span class="sxs-lookup"><span data-stu-id="b9915-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="b9915-147">\-o- (también se muestra la sintaxis alternativa para **la propiedad Value)**</span><span class="sxs-lookup"><span data-stu-id="b9915-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="b9915-148">Tipos de datos específicos de COM</span><span class="sxs-lookup"><span data-stu-id="b9915-148">COM-specific data types</span></span>

<span data-ttu-id="b9915-p114">En general, cualquier tipo de datos de Visual Basic que se encuentra en la Referencia de la API de ADO tiene un equivalente en Visual C++. Éstos incluyen tipos de datos estándar, tales como **unsigned char** para un **Byte** de Visual Basic, **short** para **Integer** y **long** para **Long**. Busque en los Índices de la sintaxis para ver qué se requiere exactamente para los operandos de un método o una propiedad dados.</span><span class="sxs-lookup"><span data-stu-id="b9915-p114">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent. These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**. Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="b9915-152">Las excepciones a esta regla son los tipo de datos específicos de COM: **Variant**, **BSTR** y **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="b9915-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="b9915-153">Variant</span><span class="sxs-lookup"><span data-stu-id="b9915-153">Variant</span></span>

<span data-ttu-id="b9915-p115">Un **Variant** es un tipo de datos estructurados que contiene un miembro de valor y un miembro de tipo de datos. Un **Variant** puede contener una amplia variedad de otros tipos de datos, incluidos otro Variant, BSTR, Boolean, IDispatch, puntero a IUnknown, moneda, fecha, etc. COM también proporciona métodos que facilitan la conversión de un tipo de datos en otro.</span><span class="sxs-lookup"><span data-stu-id="b9915-p115">A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="b9915-157">La **\_ clase variant \_ t** encapsula y administra el tipo de datos **Variant.**</span><span class="sxs-lookup"><span data-stu-id="b9915-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="b9915-158">Cuando la referencia de api de ADO indica que un operando de método o propiedad toma un valor, normalmente significa que el valor se pasa en **\_ una variante \_ t**.</span><span class="sxs-lookup"><span data-stu-id="b9915-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="b9915-p116">Esta regla se cumple explícitamente cuando la sección **Parámetros** de los temas de la Referencia de la API de ADO indica que un operando es de tipo **Variant**. Una excepción es cuando la documentación indica explícitamente que el operandos toma un tipo de datos estándar, como **Long**, **Byte** o una enumeración. Otra excepción es cuando el operando toma un **String**.</span><span class="sxs-lookup"><span data-stu-id="b9915-p116">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="b9915-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="b9915-162">BSTR</span></span>

<span data-ttu-id="b9915-p117">Un **BSTR** (**B** asic **STR** ing) es un tipo de datos estructurados que contiene una cadena de caracteres y la longitud de la cadena. COM proporciona métodos para asignar, manipular y liberar un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="b9915-p117">A **BSTR** (**B** asic **STR** ing) is a structured data type that contains a character string and the string's length. COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="b9915-165">La **\_ clase bstr \_ t** encapsula y administra el **tipo de datos BSTR.**</span><span class="sxs-lookup"><span data-stu-id="b9915-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="b9915-166">Cuando la referencia de api de ADO indica que un método o propiedad toma un valor **string,** significa que el valor está en forma de **\_ bstr \_ t**.</span><span class="sxs-lookup"><span data-stu-id="b9915-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a><span data-ttu-id="b9915-167">Conversión \_ de clases variant t y \_ \_ bstr \_ t</span><span class="sxs-lookup"><span data-stu-id="b9915-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="b9915-168">A menudo no es necesario codificar explícitamente una **\_ variante \_ t** o **\_ bstr \_ t** en un argumento a una operación.</span><span class="sxs-lookup"><span data-stu-id="b9915-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="b9915-169">Si la **\_ clase variant \_ t** o **\_ bstr \_ t** tiene un constructor que coincide con el tipo de datos del argumento, el compilador generará la variante **\_ \_ t** o **\_ bstr \_ t apropiadas.**</span><span class="sxs-lookup"><span data-stu-id="b9915-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="b9915-170">Sin embargo, si el argumento es ambiguo, es decir, el tipo de datos del argumento coincide con más de un constructor, deberá convertir el argumento explícitamente al tipo de datos apropiado para llamar al constructor correcto.</span><span class="sxs-lookup"><span data-stu-id="b9915-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="b9915-171">Por ejemplo, la declaración para el método **Recordset::Open** es:</span><span class="sxs-lookup"><span data-stu-id="b9915-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="b9915-172">El argumento ActiveConnection hace referencia a una variante **\_ \_ t**, que puede codificar como una cadena de conexión o un puntero a un **objeto Connection** abierto.</span><span class="sxs-lookup"><span data-stu-id="b9915-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="b9915-173">La variante **\_ \_ correcta t** se construirá implícitamente si pasa una cadena como "DSN=pubs;uid=sa;pwd=;", o un puntero como "(IDispatch ) \* pConn".</span><span class="sxs-lookup"><span data-stu-id="b9915-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="b9915-174">O puede codificar explícitamente una variante **\_ \_ que** contenga un puntero como " \_ variant \_ t((IDispatch \* ) pConn, true)".</span><span class="sxs-lookup"><span data-stu-id="b9915-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="b9915-175">La conversión ( IDispatch ), resuelve la ambigüedad con otro constructor que toma un \* puntero a una interfaz IUnknown.</span><span class="sxs-lookup"><span data-stu-id="b9915-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="b9915-p120">Es un hecho crucial (aunque raramente mencionado) que ADO es una interfaz IDispatch. Siempre que un puntero a un objeto ADO se deba pasar como un **Variant**, es necesario convertir explícitamente ese puntero a un puntero a un interfaz IDispatch.</span><span class="sxs-lookup"><span data-stu-id="b9915-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="b9915-178">El último caso codifica explícitamente el segundo argumento booleano del constructor con su valor predeterminado opcional true.</span><span class="sxs-lookup"><span data-stu-id="b9915-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="b9915-179">Este argumento hace que el constructor **Variant** llame a su **método AddRef**(), que compensa la llamada automática de ADO al método **\_ variant \_ t::Release**() cuando se completa el método ADO o la llamada a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b9915-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="b9915-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="b9915-180">SafeArray</span></span>

<span data-ttu-id="b9915-p122">Un **SafeArray** es un tipo de datos estructurados que contiene una matriz de otros tipos de datos. Un **SafeArray** se denomina *safe* (seguro) debido a que contiene información sobre los límites de cada dimensión de la matriz y limita el acceso a los elementos de la matriz a esos límites.</span><span class="sxs-lookup"><span data-stu-id="b9915-p122">A **SafeArray** is a structured data type that contains an array of other data types. A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="b9915-183">Cuando la Referencia de la API de ADO indica que un método o una propiedad acepta o devuelve una matriz, significa que el método o la propiedad acepta o devuelve un **SafeArray** no una matriz nativa de C/C++.</span><span class="sxs-lookup"><span data-stu-id="b9915-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="b9915-p123">Por ejemplo, el segundo parámetro del método **OpenSchema** del objeto **Conection** requiere una matriz de valores **Variant**. Esos valores **Variant** se deben pasar como elementos de un **SafeArray**, y ese **SafeArray** se debe establecer como el valor de otro **Variant**. Es ese otro **Variant** el que se pasa como el segundo argumento de **OpenSchema**.</span><span class="sxs-lookup"><span data-stu-id="b9915-p123">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values. Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**. It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="b9915-187">Como ejemplos adicionales, el primer argumento del método **Find** es un **Variant** cuyo valor es un **SafeArray** unidimensional, cada uno de los argumentos primero y segundo opcionales de **AddNew** es un **SafeArray** unidimensional y el valor devuelto del método **GetRows** es un **Variant** cuyo valor es un **SafeArray** bidimensional.</span><span class="sxs-lookup"><span data-stu-id="b9915-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="b9915-188">Parámetros faltantes y predeterminados</span><span class="sxs-lookup"><span data-stu-id="b9915-188">Missing and default parameters</span></span>

<span data-ttu-id="b9915-p124">Visual Basic permite que falten parámetros en los métodos. Por ejemplo, el método **Open** de un objeto **Recordset** tiene cinco parámetros, pero se pueden omitir parámetros intermedios y no incluir parámetros finales. Se usará entonces un **BSTR** o **Variant** predeterminado según el tipo de datos del operando que falte.</span><span class="sxs-lookup"><span data-stu-id="b9915-p124">Visual Basic allows missing parameters in methods. For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters. A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="b9915-192">En C/C++, se deben especificar todos los operandos.</span><span class="sxs-lookup"><span data-stu-id="b9915-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="b9915-193">Si desea especificar un parámetro que falta cuyo tipo de datos es una cadena, especifique un **\_ bstr \_ t** que contenga una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="b9915-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="b9915-194">Si desea especificar un parámetro que falta cuyo tipo de datos es **Variant**, especifique una variante **\_ \_ t** con un valor de DISP \_ E PARAMNOTFOUND y un tipo \_ de ERROR \_ VT.</span><span class="sxs-lookup"><span data-stu-id="b9915-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="b9915-195">Como alternativa, especifique la constante **\_ \_ t de** variante equivalente, **vtMissing**, que proporciona la directiva **\# de** importación.</span><span class="sxs-lookup"><span data-stu-id="b9915-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="b9915-p126">Existen tres métodos que constituyen excepciones al uso típico de **vtMissing**. Éstos son los métodos **Execute** de los objetos **Connection** y **Command**, y el método **NextRecordset** del objeto **Recordset**. Las siguientes son sus firmas:</span><span class="sxs-lookup"><span data-stu-id="b9915-p126">Three methods are exceptions to the typical use of **vtMissing**. These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object. The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="b9915-p127">Los parámetros *RecordsAffected* y *Parameters* son punteros a un **Variant**. *Parameters* es un parámetro de entrada que especifica la dirección de un **Variant** que contiene un parámetro único, o una matriz de parámetros, que modificará el comando que se va a ejecutar. *RecordsAffected* es un parámetro de salida que especifica la dirección de un **Variant** donde se devuelve el número de filas afectadas por el método.</span><span class="sxs-lookup"><span data-stu-id="b9915-p127">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**. *Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed. *RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="b9915-202">En el **método Execute** del objeto **Command,** indique que no se especifica ningún parámetro estableciendo *Parameters* en vtMissing (que se recomienda) o en el puntero \& nulo (es decir, **NULL** o cero (0)).</span><span class="sxs-lookup"><span data-stu-id="b9915-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="b9915-203">Si *Parameters* se establece en el puntero nulo, el método sustituye internamente el equivalente de **vtMissing** y, a continuación, completa la operación.</span><span class="sxs-lookup"><span data-stu-id="b9915-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="b9915-p129">En todos los métodos, indique que no se debe devolver el número de registros afectados; puede hacerlo estableciendo *RecordsAffected* en un puntero nulo. En este caso, el puntero nulo no es tanto un parámetro que falta como una indicación de que el método debería descartar el número de registros afectados.</span><span class="sxs-lookup"><span data-stu-id="b9915-p129">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer. In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="b9915-206">Por tanto, para estos tres métodos, es correcto codificar del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="b9915-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="b9915-207">Control de errores</span><span class="sxs-lookup"><span data-stu-id="b9915-207">Error handling</span></span>

<span data-ttu-id="b9915-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span><span class="sxs-lookup"><span data-stu-id="b9915-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="b9915-209">La **\# directiva import** genera código contenedor alrededor de cada método o propiedad "sin procesar" y comprueba el HRESULT devuelto.</span><span class="sxs-lookup"><span data-stu-id="b9915-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="b9915-210">Si el HRESULT indica un error, el código contenedor genera un error COM llamando a \_ \_ com issue errorex() con el código devuelto \_ HRESULT como argumento.</span><span class="sxs-lookup"><span data-stu-id="b9915-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="b9915-211">COM error objects can be caught in a **try**-**catch** block.</span><span class="sxs-lookup"><span data-stu-id="b9915-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="b9915-212">(Por razones de eficiencia, captura una referencia a un **\_ objeto de \_ error com).**</span><span class="sxs-lookup"><span data-stu-id="b9915-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="b9915-p131">Recuerde que éstos son errores de ADO (resultado de una operación ADO). Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="b9915-p131">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="b9915-215">La **\# directiva import** crea solo rutinas de control de errores para métodos y propiedades declarados en el .dll ADO.</span><span class="sxs-lookup"><span data-stu-id="b9915-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="b9915-216">Sin embargo, puede aprovechar este mismo mecanismo de tratamiento de errores escribiendo su propia función en línea o macro de comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="b9915-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="b9915-217">Vea el tema [Extensiones de Visual C++](visual-c-extensions-for-ado.md) o el código de la sección siguiente para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="b9915-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="b9915-218">Equivalentes de Visual C++ de Visual Basic convenciones</span><span class="sxs-lookup"><span data-stu-id="b9915-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="b9915-219">A continuación, se muestra un resumen de diversas convenciones de la documentación de ADO, codificadas en Visual Basic, así como sus equivalentes en Visual C++.</span><span class="sxs-lookup"><span data-stu-id="b9915-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="b9915-220">Declaración de un objeto ADO</span><span class="sxs-lookup"><span data-stu-id="b9915-220">Declaring an ADO object</span></span>

<span data-ttu-id="b9915-221">En Visual Basic, una variable de objeto ADO (en este caso, de un objeto **Recordset**) se declara del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="b9915-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="b9915-222">La cláusula, "ADODB. Recordset", es el ProgID del **objeto Recordset** tal como se define en el Registro.</span><span class="sxs-lookup"><span data-stu-id="b9915-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="b9915-223">Una instancia nueva de un objeto **Record** se declara del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="b9915-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="b9915-224">\-o-</span><span class="sxs-lookup"><span data-stu-id="b9915-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="b9915-225">En Visual C++, la **\# directiva import** genera declaraciones de tipo puntero inteligentes para todos los objetos ADO.</span><span class="sxs-lookup"><span data-stu-id="b9915-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="b9915-226">Por ejemplo, una variable que apunta a un **\_ objeto Recordset** es de tipo **\_ RecordsetPtr** y se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b9915-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="b9915-227">A variable that points to a new instance of a **\_ Recordset** object is declared as follows:</span><span class="sxs-lookup"><span data-stu-id="b9915-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="b9915-228">\-o-</span><span class="sxs-lookup"><span data-stu-id="b9915-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="b9915-229">\-o-</span><span class="sxs-lookup"><span data-stu-id="b9915-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="b9915-230">Después de llamar al método **CreateInstance**, la variable se puede utilizar de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="b9915-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="b9915-231">Observe que, en un caso, el operador "." se usa como si la variable fuera una instancia de una clase (rs. CreateInstance) y, en otro caso, el operador "- " se usa como si la variable fuera un puntero a una \> interfaz (rs- \> Open).</span><span class="sxs-lookup"><span data-stu-id="b9915-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="b9915-232">Una variable se puede usar de dos maneras porque el operador "- " está sobrecargado para permitir que una instancia de una clase se comporte como un puntero \> a una interfaz.</span><span class="sxs-lookup"><span data-stu-id="b9915-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="b9915-233">Un miembro de clase privada de la variable de instancia contiene un puntero a la interfaz **\_ Recordset;** el operador "- " devuelve ese puntero y el puntero devuelto tiene acceso a los miembros del \> **\_ objeto Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b9915-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="b9915-234">Codificar un parámetro que falta</span><span class="sxs-lookup"><span data-stu-id="b9915-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="b9915-235">Cadena</span><span class="sxs-lookup"><span data-stu-id="b9915-235">String</span></span>

<span data-ttu-id="b9915-236">Cuando necesite codificar en Visual Basic un operando **String** ausente, simplemente omita el operando.</span><span class="sxs-lookup"><span data-stu-id="b9915-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="b9915-237">Deberá especificar el operando en Visual C++.</span><span class="sxs-lookup"><span data-stu-id="b9915-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="b9915-238">Codificar **\_ un bstr \_ t** que tenga una cadena vacía como valor.</span><span class="sxs-lookup"><span data-stu-id="b9915-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="b9915-239">Variant</span><span class="sxs-lookup"><span data-stu-id="b9915-239">Variant</span></span>

<span data-ttu-id="b9915-240">Cuando necesite codificar en Visual Basic un operando **Variant** ausente, simplemente omita el operando.</span><span class="sxs-lookup"><span data-stu-id="b9915-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="b9915-241">En Visual C++, deberá especificar todos los operandos.</span><span class="sxs-lookup"><span data-stu-id="b9915-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="b9915-242">Codifica un parámetro **Variant** que falta con una **\_ variante \_ t** establecida en el valor especial, DISP \_ E \_ PARAMNOTFOUND y type, VT \_ ERROR.</span><span class="sxs-lookup"><span data-stu-id="b9915-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="b9915-243">Como alternativa, especifique **vtMissing**, que es una constante predefinida equivalente suministrada por la **\# directiva de** importación.</span><span class="sxs-lookup"><span data-stu-id="b9915-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="b9915-244">\-o usar -</span><span class="sxs-lookup"><span data-stu-id="b9915-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="b9915-245">Declaración de una variante</span><span class="sxs-lookup"><span data-stu-id="b9915-245">Declaring a variant</span></span>

<span data-ttu-id="b9915-246">En Visual Basic, un tipo **Variant** se declara con la instrucción **Dim** del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="b9915-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="b9915-247">En Visual C++, declare una variable como tipo **\_ variant \_ t**.</span><span class="sxs-lookup"><span data-stu-id="b9915-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="b9915-248">A continuación se muestran algunas declaraciones de variante **\_ \_ t** esquemáticas.</span><span class="sxs-lookup"><span data-stu-id="b9915-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="b9915-p139">Estas declaraciones simplemente proporcionan una idea general de cómo podría codificar su propio programa. Para obtener más información, vea los ejemplos siguientes y la documentación de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="b9915-p139">These declarations merely give a rough idea of what you would code in your own program. For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="b9915-251">Uso de matrices de variantes</span><span class="sxs-lookup"><span data-stu-id="b9915-251">Using arrays of variants</span></span>

<span data-ttu-id="b9915-252">En Visual Basic, las matrices de **Variants** se pueden codificar con la instrucción **Dim** o utilizar la función **Array**, tal como se muestra en el código de ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b9915-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

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

<span data-ttu-id="b9915-253">En el siguiente ejemplo de Visual C++ se muestra el uso de **un SafeArray** usado con **\_ una variante \_ t**.</span><span class="sxs-lookup"><span data-stu-id="b9915-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="b9915-254">Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b9915-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="b9915-255">Una vez más, se define la función inline TESTHR() para aprovechar el mecanismo de control de errores existente.</span><span class="sxs-lookup"><span data-stu-id="b9915-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="b9915-p140">Sólo necesitará una matriz unidimensional, de forma que pueda utilizar **SafeArrayCreateVector** en lugar de la declaración de propósito general **SAFEARRAYBOUND** y la función **SafeArrayCreate**. El código que utiliza **SafeArrayCreate** tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="b9915-p140">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function. The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="b9915-258">El esquema identificado por la constante enumerada, **adSchemaColumns**, está asociado a cuatro columnas de restricción: TABLE \_ CATALOG, TABLE \_ SCHEMA, TABLE \_ NAME y COLUMN \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="b9915-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="b9915-259">Por lo tanto, se crea una matriz de valores **Variant** con cuatro elementos.</span><span class="sxs-lookup"><span data-stu-id="b9915-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="b9915-260">A continuación, se especifica un valor de restricción que corresponde a la tercera columna, NOMBRE DE \_ TABLA.</span><span class="sxs-lookup"><span data-stu-id="b9915-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="b9915-261">El objeto **Recordset** que se devuelve consta de varias columnas, entre las que se incluyen las columnas de restricción.</span><span class="sxs-lookup"><span data-stu-id="b9915-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="b9915-262">Los valores de las columnas de restricción para cada fila devuelta deben ser los mismos que los valores de restricción correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b9915-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="b9915-263">Aquéllos familiarizados con **SafeArrays** se pueden sorprender del hecho de que no se llame a **SafeArrayDestroy**() antes de la salida.</span><span class="sxs-lookup"><span data-stu-id="b9915-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="b9915-264">De hecho, llamar a **SafeArrayDestroy**() provocará en este caso una excepción en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b9915-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="b9915-265">El motivo es que el destructor de vtCriteria llamará **a VariantClear**() cuando la variante **\_ \_ t** se salga del ámbito, lo que liberará **safearray**.</span><span class="sxs-lookup"><span data-stu-id="b9915-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="b9915-266">Llamar **a SafeArrayDestroy**, sin borrar manualmente la variante **\_ \_ t**, haría que el destructor intentara borrar un puntero **SafeArray** no válido.</span><span class="sxs-lookup"><span data-stu-id="b9915-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="b9915-267">Si se hiciera la llamada a **SafeArrayDestroy**, el código presentaría el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="b9915-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="b9915-268">Sin embargo, es mucho más sencillo permitir que la **\_ variante \_ t** administre **safearray**.</span><span class="sxs-lookup"><span data-stu-id="b9915-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


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

### <a name="using-property-getputputref"></a><span data-ttu-id="b9915-269">Uso de la propiedad Get/Put/PutRef</span><span class="sxs-lookup"><span data-stu-id="b9915-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="b9915-270">En Visual Basic, el nombre de una propiedad no indica si ésta se ha recuperado, si se le ha asignado un valor o se le ha asignado una referencia.</span><span class="sxs-lookup"><span data-stu-id="b9915-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

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

<span data-ttu-id="b9915-271">En este ejemplo de Visual C++ se muestra **la propiedad Get** / **Put** /\* *PutRef\*\*\*.*</span><span class="sxs-lookup"><span data-stu-id="b9915-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="b9915-272">Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b9915-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="b9915-273">En este ejemplo se usan dos formas de argumento de cadena que faltan: una constante explícita, **strMissing** y una cadena que el compilador usará para crear una **\_ bstr \_ t temporal** que existirá para el ámbito del método **Open.**</span><span class="sxs-lookup"><span data-stu-id="b9915-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="b9915-274">No es necesario convertir el operando de rs- \> PutRefActiveConnection(cn) en (IDispatch ) porque el tipo del operando ya \* es (IDispatch \* ).</span><span class="sxs-lookup"><span data-stu-id="b9915-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
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

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="b9915-275">Uso de GetItem(x) y Item \[ x\]</span><span class="sxs-lookup"><span data-stu-id="b9915-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="b9915-276">Este ejemplo de Visual Basic muestra la sintaxis estándar y alternativa para **Item**().</span><span class="sxs-lookup"><span data-stu-id="b9915-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

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

<span data-ttu-id="b9915-277">En este ejemplo de Visual C++, se muestra el uso de **Item**.</span><span class="sxs-lookup"><span data-stu-id="b9915-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="b9915-278">[!NOTA] La nota siguiente corresponde a secciones comentadas en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b9915-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="b9915-279">Cuando se obtiene acceso a la colección mediante **Item**, el índice, **2**, se debe convertir explícitamente a **long** para que se realice la llamada al constructor apropiado.</span><span class="sxs-lookup"><span data-stu-id="b9915-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="b9915-280">Conversión de punteros de objeto ADO con (IDispatch \* )</span><span class="sxs-lookup"><span data-stu-id="b9915-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="b9915-281">El siguiente ejemplo de Visual C++ muestra el uso de ( IDispatch \* ) para convertir explícitamente punteros a objetos ADO.</span><span class="sxs-lookup"><span data-stu-id="b9915-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="b9915-282">[!NOTA] Las notas siguientes corresponden a secciones comentadas en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b9915-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="b9915-283">Especifique un objeto **Connection** abierto en un **Variant** codificado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="b9915-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="b9915-284">Cast it with (IDispatch \* ) so the correct constructor will be invoked.</span><span class="sxs-lookup"><span data-stu-id="b9915-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="b9915-285">Además, establezca explícitamente el segundo parámetro **\_ variant \_ t** en el valor predeterminado de **true,** por lo que el recuento de referencias de objeto será correcto cuando finalice la operación **Recordset::Open.**</span><span class="sxs-lookup"><span data-stu-id="b9915-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="b9915-286">La expresión , ( bstr t), no es una conversión, sino un operador variant t que extrae una cadena \_ \_ **\_ bstr \_ t** **\_ \_** de **variant** devuelta por **Value**.</span><span class="sxs-lookup"><span data-stu-id="b9915-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="b9915-287">La expresión ( char ), no es una conversión, sino un operador bstr t que extrae un puntero a la cadena \* encapsulada en un **\_ objeto bstr \_ t.** **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9915-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="b9915-288">Esta sección de código muestra algunos de los comportamientos útiles de **\_ los operadores variant \_ t** y **\_ bstr \_ t.**</span><span class="sxs-lookup"><span data-stu-id="b9915-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
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

