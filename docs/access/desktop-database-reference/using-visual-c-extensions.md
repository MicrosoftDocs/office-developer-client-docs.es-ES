---
title: Utilizar Extensiones de Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcfde7e343a37d65356e1f9ed8d879030913f5ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868787"
---
# <a name="using-visual-c-extensions"></a><span data-ttu-id="50269-102">Utilizar Extensiones de Visual C++</span><span class="sxs-lookup"><span data-stu-id="50269-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="50269-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50269-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="50269-104">Interfaz IADORecordBinding</span><span class="sxs-lookup"><span data-stu-id="50269-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="50269-p101">Las Extensiones de Microsoft Visual C++ para ADO asocian o enlazan los campos de un objeto [Recordset](recordset-object-ado.md) a las variables de C/C++. Cuando cambia la actual fila del objeto **Recordset** enlazado, todos los campos enlazados del objeto **Recordset** se copian en las variables de C/C++. Si es necesario, los datos copiados se convierten en el tipo de datos declarado de la variable de C/C++.</span><span class="sxs-lookup"><span data-stu-id="50269-p101">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables. If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="50269-p102">El método **BindToRecordset** de la interfaz **IADORecordBinding** asocia los campos a las variables de C/C++. El método **AddNew** agrega una fila nueva al objeto **Recordset** enlazado. El método **Update** rellena los campos en las nuevas filas del objeto **Recordset** o actualiza los campos en las filas existentes con el valor de las variables de C/C++.</span><span class="sxs-lookup"><span data-stu-id="50269-p102">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables. The **AddNew** method adds a new row to the bound **Recordset**. The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="50269-p103">La interfaz **IADORecordBinding** la implementa el objeto **Recordset**. La implementación no se realiza mediante código del usuario.</span><span class="sxs-lookup"><span data-stu-id="50269-p103">The **IADORecordBinding** interface is implemented by the **Recordset** object. You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="50269-113">Entradas de enlace</span><span class="sxs-lookup"><span data-stu-id="50269-113">Binding Entries</span></span>

<span data-ttu-id="50269-p104">Las Extensiones de Visual C++ para ADO asignan los campos de un objeto [Recordset](recordset-object-ado.md) a las variables de C/C++. La definición de una asignación entre un campo y una variable se denomina *entrada de enlace*. Las macros proporcionan entradas de enlace para los datos numéricos, datos de longitud fija y de longitud variable. Las entradas de enlace y las variables de C/C++ se declaran en una clase derivada de la clase **CADORecordBinding** de Extensiones de Visual C++. La clase **CADORecordBinding** la definen internamente las macros de entradas de enlace.</span><span class="sxs-lookup"><span data-stu-id="50269-p104">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. The definition of a mapping between a field and a variable is called a *binding entry*. Macros provide binding entries for numeric, fixed-length, and variable-length data. The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**. The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="50269-p105">ADO asigna internamente los parámetros de estas macros a una estructura **DBBINDING** de OLE DB y crea un objeto **Accessor** de OLE DB para administrar el movimiento y la conversión de los datos entre los campos y las variables. OLE DB define los datos como datos que se componen de tres partes: un *búfer* donde se almacenan los datos, un *estado* que indica si un campo se ha almacenado correctamente en el búfer o cómo debe restaurarse la variable en el campo, y la *longitud* de los datos. (Si desea obtener más información, vea el Capítulo 6 de *Referencia del programador de OLE DB*: Obtener y establecer datos.)</span><span class="sxs-lookup"><span data-stu-id="50269-p105">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables. OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data. (See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="50269-122">Archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="50269-122">Header File</span></span>

<span data-ttu-id="50269-123">Incluya el archivo siguiente en la aplicación para que pueda utilizar las Extensiones de Visual C++ para ADO:</span><span class="sxs-lookup"><span data-stu-id="50269-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="50269-124">Enlazar campos del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="50269-124">Binding Recordset Fields</span></span>

<span data-ttu-id="50269-125">**Para enlazar campos del objeto Recordset a las variables de C/C++**</span><span class="sxs-lookup"><span data-stu-id="50269-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="50269-126">Cree una clase derivada de la clase **CADORecordBinding**.</span><span class="sxs-lookup"><span data-stu-id="50269-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="50269-127">Especifique las entradas de enlace y las correspondientes variables de C/C++ en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="50269-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="50269-128">Inserte las entradas de enlace entre **comenzar\_ADO\_enlace** y **END\_ADO\_enlace** las macros.</span><span class="sxs-lookup"><span data-stu-id="50269-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="50269-129">No termine las macros con comas ni signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="50269-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="50269-130">Cada macro especifica automáticamente los delimitadores apropiados.</span><span class="sxs-lookup"><span data-stu-id="50269-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="50269-131">Especifique una entrada de enlace por cada campo que se va a asignar a una variable de C/C++.</span><span class="sxs-lookup"><span data-stu-id="50269-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="50269-132">Utilice un miembro apropiado de la **ADO\_fijo\_longitud\_entrada**, **ADO\_numérico\_entrada**, o **ADO\_VARIABLE\_longitud\_entrada** familia de macros.</span><span class="sxs-lookup"><span data-stu-id="50269-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="50269-p107">En la aplicación, cree una instancia de la clase derivada de **CADORecordBinding**. Obtenga la interfaz **IADORecordBinding** del objeto **Recordset**. A continuación, llame al método **BindToRecordset** para asociar los campos del objeto **Recordset** a las variables de C/C++.</span><span class="sxs-lookup"><span data-stu-id="50269-p107">In your application, create an instance of the class derived from **CADORecordBinding**. Get the **IADORecordBinding** interface from the **Recordset**. Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="50269-136">Vea [Ejemplo de Extensiones de Visual C++](visual-c-extensions-example.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="50269-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="50269-137">Métodos de interfaz</span><span class="sxs-lookup"><span data-stu-id="50269-137">Interface Methods</span></span>

<span data-ttu-id="50269-p108">La interfaz **IADORecordBinding** tiene tres métodos: **BindToRecordset**, **AddNew** y **Update**. El único argumento de cada método es un puntero a una instancia de la clase derivada de **CADORecordBinding**. Por lo tanto, los métodos **AddNew** y **Update** no pueden especificar ninguno de los parámetros de los homónimos de ADO de sus métodos.</span><span class="sxs-lookup"><span data-stu-id="50269-p108">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**. The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**. Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="50269-141">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="50269-141">**Syntax**</span></span>

<span data-ttu-id="50269-142">El método **BindToRecordset** asocia los campos del objeto **Recordset** a las variables de C/C++.</span><span class="sxs-lookup"><span data-stu-id="50269-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="50269-143">El método **AddNew** invoca su homónimo, el método [AddNew](addnew-method-ado.md) de ADO, para agregar una fila nueva al objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="50269-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="50269-144">El método **Update** invoca su homónimo, el método [Update](update-method-ado.md) de ADO, para actualizar el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="50269-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="50269-145">Macros de entradas de enlace</span><span class="sxs-lookup"><span data-stu-id="50269-145">Binding Entry Macros</span></span>

<span data-ttu-id="50269-p109">Las macros de entradas de enlace definen la asociación de un campo del objeto **Recordset** y una variable. Una macro inicial y una macro final delimitan el conjunto de entradas de enlace.</span><span class="sxs-lookup"><span data-stu-id="50269-p109">Binding entry macros define the association of a **Recordset** field and a variable. A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="50269-p110">Hay familias de macros para datos de longitud fija, como **adDate** o **adBoolean**, datos numéricos como **adTinyInt**, **adInteger** o **adDouble**, y datos de longitud variable como **adChar**, **adVarChar** o **adVarBinary**. Todos los tipos numéricos, excepto **adVarNumeric**, son también tipos de longitud fija. Cada familia tiene diferentes conjuntos de parámetros de modo que se puede excluir la información de enlace que no sea de interés.</span><span class="sxs-lookup"><span data-stu-id="50269-p110">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**. All numeric types, except for **adVarNumeric**, are also fixed-length types. Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="50269-151">Vea los tipos de datos de *referencia del programador de OLE DB,* Apéndice A: para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="50269-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="50269-152">_**Comenzar entradas de enlace**_</span><span class="sxs-lookup"><span data-stu-id="50269-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="50269-153">**COMENZAR\_ADO\_enlace**(*clase*)</span><span class="sxs-lookup"><span data-stu-id="50269-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="50269-154">_**Datos de longitud fija**_</span><span class="sxs-lookup"><span data-stu-id="50269-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="50269-155">**ADO\_fijo\_longitud\_entrada**(*Ordinal, el tipo de datos, el búfer, el estado, modificar*)</span><span class="sxs-lookup"><span data-stu-id="50269-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="50269-156">**ADO\_fijo\_longitud\_ENTRY2**(*Ordinal, el tipo de datos, el búfer, modificar*)</span><span class="sxs-lookup"><span data-stu-id="50269-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="50269-157">_**Datos numéricos**_</span><span class="sxs-lookup"><span data-stu-id="50269-157">_**Numeric Data**_</span></span>

<span data-ttu-id="50269-158">**ADO\_numérico\_entrada**(*Ordinal, tipo de datos, búfer, precisión, escala, estado, modificar*)</span><span class="sxs-lookup"><span data-stu-id="50269-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="50269-159">**ADO\_numérico\_ENTRY2**(*Ordinal, tipo de datos, búfer, precisión, escala, modificar*)</span><span class="sxs-lookup"><span data-stu-id="50269-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="50269-160">_**Datos de longitud variable**_</span><span class="sxs-lookup"><span data-stu-id="50269-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="50269-161">**ADO\_VARIABLE\_longitud\_entrada**(*Ordinal, tipo de datos, búfer, tamaño, estado, longitud, modificar*)</span><span class="sxs-lookup"><span data-stu-id="50269-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="50269-162">**ADO\_VARIABLE\_longitud\_ENTRY2**(*Ordinal, tipo de datos, búfer, tamaño, estado, modificar*)</span><span class="sxs-lookup"><span data-stu-id="50269-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="50269-163">**ADO\_VARIABLE\_longitud\_Entrada3**(*Ordinal, tipo de datos, búfer, tamaño, longitud, modificar*)</span><span class="sxs-lookup"><span data-stu-id="50269-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="50269-164">**ADO\_VARIABLE\_longitud\_Entrada4**(*Ordinal, el tipo de datos, el búfer, el tamaño, modificar*)</span><span class="sxs-lookup"><span data-stu-id="50269-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="50269-165">_**End entradas de enlace**_</span><span class="sxs-lookup"><span data-stu-id="50269-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="50269-166">**END\_ADO\_enlace** ()</span><span class="sxs-lookup"><span data-stu-id="50269-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50269-167">Parámetro</span><span class="sxs-lookup"><span data-stu-id="50269-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="50269-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="50269-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50269-169"><em>Class</em></span><span class="sxs-lookup"><span data-stu-id="50269-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="50269-170">Clase en la que se definen las entradas de enlace y las variables de C/C++.</span><span class="sxs-lookup"><span data-stu-id="50269-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-171"><em>Ordinal</em></span><span class="sxs-lookup"><span data-stu-id="50269-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="50269-172">Número ordinal, a partir de 1, del campo del objeto <strong>Recordset</strong> correspondiente a la variable de C/C++.</span><span class="sxs-lookup"><span data-stu-id="50269-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="50269-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="50269-p111">Tipo de datos de ADO equivalente de la variable de C/C++ (vea <a href="datatypeenum.md">DataTypeEnum</a> para obtener una lista de tipos de datos válidos). El valor del campo del objeto <strong>Recordset</strong> se convertirá en este tipo de datos si es necesario.</span><span class="sxs-lookup"><span data-stu-id="50269-p111">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types). The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-176"><em>Buffer</em></span><span class="sxs-lookup"><span data-stu-id="50269-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="50269-177">Nombre de la variable de C/C++ donde se almacenará el campo del objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="50269-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-178"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="50269-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="50269-p112">Tamaño máximo, en bytes, de <em>Buffer</em>. Si <em>Buffer</em> va a contener una cadena de longitud variable, deje espacio para un cero final.</span><span class="sxs-lookup"><span data-stu-id="50269-p112">Maximum size in bytes of <em>Buffer</em>. If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-181"><em>Status</em></span><span class="sxs-lookup"><span data-stu-id="50269-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="50269-182">Nombre de una variable que va a indicar si el contenido de <em>Buffer</em> es válido y si la conversión del campo en <em>DataType</em> se ha realizado correctamente.
</span><span class="sxs-lookup"><span data-stu-id="50269-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="50269-183">Los dos valores más importantes de esta variable son <strong>adFldOK</strong> y <strong>adFldNull</strong>, es decir, la conversión se ha realizado correctamente y el valor del campo es VARIANT de tipo VT_NULL y no está vacío, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="50269-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="50269-184">Los posibles valores de <em>estado</em> se enumeran en la tabla siguiente, &quot;valores de estado.&quot;</span><span class="sxs-lookup"><span data-stu-id="50269-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-185"><em>Modificar</em></span><span class="sxs-lookup"><span data-stu-id="50269-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="50269-186">Marca de operador booleano. Si su valor es TRUE, indica que ADO puede actualizar el correspondiente campo de <strong>Recordset</strong> con el valor de <em>Buffer</em>.
</span><span class="sxs-lookup"><span data-stu-id="50269-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="50269-187">Establezca el valor del parámetro booleano <em>Modify</em> en TRUE para que ADO pueda actualizar el campo enlazado. Establézcalo en FALSE si desea examinar el campo sin cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="50269-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-188"><em>Precision</em></span><span class="sxs-lookup"><span data-stu-id="50269-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="50269-189">Número de dígitos que se pueden representar en una variable numérica.</span><span class="sxs-lookup"><span data-stu-id="50269-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-190"><em>Scale</em></span><span class="sxs-lookup"><span data-stu-id="50269-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="50269-191">Número de posiciones de decimales en una variable numérica.</span><span class="sxs-lookup"><span data-stu-id="50269-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-192"><em>Length</em></span><span class="sxs-lookup"><span data-stu-id="50269-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="50269-193">Nombre de una variable de cuatro bytes que va a contener la longitud real de los datos en <em>Buffer</em>.</span><span class="sxs-lookup"><span data-stu-id="50269-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="50269-194">Valores de Status</span><span class="sxs-lookup"><span data-stu-id="50269-194">Status Values</span></span>

<span data-ttu-id="50269-195">El valor de la variable *Status* indica si un campo se ha copiado correctamente a una variable.</span><span class="sxs-lookup"><span data-stu-id="50269-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="50269-196">Al configurar los datos, puede que el valor de *Status* sea **adFldNull** para indicar que el campo del objeto **Recordset** debe establecerse en null.</span><span class="sxs-lookup"><span data-stu-id="50269-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50269-197">Constante</span><span class="sxs-lookup"><span data-stu-id="50269-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="50269-198">Valor</span><span class="sxs-lookup"><span data-stu-id="50269-198">Value</span></span></p></th>
<th><p><span data-ttu-id="50269-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="50269-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50269-200"><strong>adFldOK</strong></span><span class="sxs-lookup"><span data-stu-id="50269-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-201">0</span><span class="sxs-lookup"><span data-stu-id="50269-201">0</span></span></p></td>
<td><p><span data-ttu-id="50269-202">Se ha devuelto un valor de campo que no sea null.</span><span class="sxs-lookup"><span data-stu-id="50269-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-203"><strong>adFldBadAccessor</strong></span><span class="sxs-lookup"><span data-stu-id="50269-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-204">1</span><span class="sxs-lookup"><span data-stu-id="50269-204">1</span></span></p></td>
<td><p><span data-ttu-id="50269-205">El enlace no es válido.</span><span class="sxs-lookup"><span data-stu-id="50269-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-206"><strong>adFldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="50269-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-207">2</span><span class="sxs-lookup"><span data-stu-id="50269-207">2</span></span></p></td>
<td><p><span data-ttu-id="50269-208">El valor no se ha podido convertir por motivos que no sean la falta de coincidencia de los signos o el desbordamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="50269-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-209"><strong>adFldNull</strong></span><span class="sxs-lookup"><span data-stu-id="50269-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-210">3</span><span class="sxs-lookup"><span data-stu-id="50269-210">3</span></span></p></td>
<td><p><span data-ttu-id="50269-211">Al obtener un campo, indica que se ha devuelto un valor null.
</span><span class="sxs-lookup"><span data-stu-id="50269-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="50269-212">Cuando establece un campo, indica que el campo debe establecerse en <strong>NULL</strong> cuando no puede codificar <strong>NULL</strong> por sí mismo (por ejemplo, una matriz de caracteres o un entero).</span><span class="sxs-lookup"><span data-stu-id="50269-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-213"><strong>adFldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="50269-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-214">4</span><span class="sxs-lookup"><span data-stu-id="50269-214">4</span></span></p></td>
<td><p><span data-ttu-id="50269-215">Se han truncado los datos de longitud variable o los dígitos numéricos.</span><span class="sxs-lookup"><span data-stu-id="50269-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-216"><strong>adFldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="50269-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-217">5</span><span class="sxs-lookup"><span data-stu-id="50269-217">5</span></span></p></td>
<td><p><span data-ttu-id="50269-218">El valor tiene signo y el tipo de datos no lo tiene.</span><span class="sxs-lookup"><span data-stu-id="50269-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-219"><strong>adFldDataOverFlow</strong></span><span class="sxs-lookup"><span data-stu-id="50269-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-220">6</span><span class="sxs-lookup"><span data-stu-id="50269-220">6</span></span></p></td>
<td><p><span data-ttu-id="50269-221">El valor es mayor que el valor que se puede almacenar en el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="50269-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-222"><strong>adFldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="50269-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-223">7</span><span class="sxs-lookup"><span data-stu-id="50269-223">7</span></span></p></td>
<td><p><span data-ttu-id="50269-224">El campo y el tipo de columna desconocidos ya están abiertos.</span><span class="sxs-lookup"><span data-stu-id="50269-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-225"><strong>adFldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="50269-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-226">8</span><span class="sxs-lookup"><span data-stu-id="50269-226">8</span></span></p></td>
<td><p><span data-ttu-id="50269-227">No se ha podido determinar el valor del campo. Por ejemplo, en un nuevo campo no asignado sin valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="50269-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-228"><strong>adFldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="50269-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-229">9</span><span class="sxs-lookup"><span data-stu-id="50269-229">9</span></span></p></td>
<td><p><span data-ttu-id="50269-230">Al actualizar, no hay permiso para escribir datos.</span><span class="sxs-lookup"><span data-stu-id="50269-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-231"><strong>adFldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="50269-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-232">10</span><span class="sxs-lookup"><span data-stu-id="50269-232">10</span></span></p></td>
<td><p><span data-ttu-id="50269-233">Al actualizar, el valor de campo infringirá la integridad de las columnas.</span><span class="sxs-lookup"><span data-stu-id="50269-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-234"><strong>adFldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="50269-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-235">11</span><span class="sxs-lookup"><span data-stu-id="50269-235">11</span></span></p></td>
<td><p><span data-ttu-id="50269-236">Al actualizar, el valor de campo infringirá el esquema de las columnas.</span><span class="sxs-lookup"><span data-stu-id="50269-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50269-237"><strong>adFldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="50269-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-238">12</span><span class="sxs-lookup"><span data-stu-id="50269-238">12</span></span></p></td>
<td><p><span data-ttu-id="50269-239">Al actualizar, parámetro de estado no válido.</span><span class="sxs-lookup"><span data-stu-id="50269-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50269-240"><strong>adFldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="50269-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="50269-241">13</span><span class="sxs-lookup"><span data-stu-id="50269-241">13</span></span></p></td>
<td><p><span data-ttu-id="50269-242">Al actualizar, se ha utilizado un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="50269-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>

