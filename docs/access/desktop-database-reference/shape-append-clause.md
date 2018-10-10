---
title: Cláusula Append del comando Shape
TOCTitle: Shape Append Clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6460572f44e79fe4bdb30d1ca33810d610da9721
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483840"
---
# <a name="shape-append-clause"></a><span data-ttu-id="f073f-102">Cláusula Append del comando Shape</span><span class="sxs-lookup"><span data-stu-id="f073f-102">Shape Append Clause</span></span>


<span data-ttu-id="f073f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f073f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f073f-p101">La cláusula APPEND del comando Shape anexa una o varias columnas a un objeto **Recordset**. Estas columnas suelen ser columnas de capítulo, que hacen referencia a un objeto secundario de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f073f-p101">The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f073f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f073f-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="f073f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f073f-107">Description</span></span>

<span data-ttu-id="f073f-108">Esta cláusula se compone de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f073f-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="f073f-109">*comando primario*</span><span class="sxs-lookup"><span data-stu-id="f073f-109">*parent-command*</span></span>

- <span data-ttu-id="f073f-110">Cero o uno de los siguientes (comandos se puede omitir el *comando a primario* en su totalidad):</span><span class="sxs-lookup"><span data-stu-id="f073f-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="f073f-p102">Un comando de proveedor entre llaves ("{}") que devuelve un objeto **Recordset**. El comando se emite al proveedor de datos subyacente y su sintaxis depende de los requisitos de ese proveedor. Suele ser el lenguaje SQL, si bien ADO no requiere ningún lenguaje de consulta en particular.</span><span class="sxs-lookup"><span data-stu-id="f073f-p102">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="f073f-114">Otro comando Shape incrustado entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="f073f-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="f073f-115">La palabra clave TABLE, seguida del nombre de una tabla en el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="f073f-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="f073f-116">*alias primario*</span><span class="sxs-lookup"><span data-stu-id="f073f-116">*parent-alias*</span></span>

  - <span data-ttu-id="f073f-117">Alias opcional que hace referencia al objeto **Recordset** primario.</span><span class="sxs-lookup"><span data-stu-id="f073f-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="f073f-118">*lista de columnas*</span><span class="sxs-lookup"><span data-stu-id="f073f-118">*column-list*</span></span>

  - <span data-ttu-id="f073f-119">Una o varias de las siguientes columnas:</span><span class="sxs-lookup"><span data-stu-id="f073f-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="f073f-120">Columna agregada.</span><span class="sxs-lookup"><span data-stu-id="f073f-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="f073f-121">Columna calculada.</span><span class="sxs-lookup"><span data-stu-id="f073f-121">A calculated column.</span></span>
    
    - <span data-ttu-id="f073f-122">Columna nueva creada con la cláusula NEW.</span><span class="sxs-lookup"><span data-stu-id="f073f-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="f073f-p103">Columna de capítulo. La definición de la columna de capítulo se encuentra entre paréntesis ("()"). Vea la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="f073f-p103">A chapter column. A chapter column definition is enclosed in parentheses ("()"). See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="f073f-126">*conjunto de registros secundario*</span><span class="sxs-lookup"><span data-stu-id="f073f-126">*child-recordset*</span></span>

  - <span data-ttu-id="f073f-p104">Un comando de proveedor entre llaves ("{}") que devuelve un objeto **Recordset**. El comando se emite al proveedor de datos subyacente y su sintaxis depende de los requisitos de ese proveedor. Suele ser el lenguaje SQL, si bien ADO no requiere ningún lenguaje de consulta en particular.</span><span class="sxs-lookup"><span data-stu-id="f073f-p104">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="f073f-130">Otro comando Shape incrustado entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="f073f-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="f073f-131">El nombre de un objeto **Recordset** con forma existente.</span><span class="sxs-lookup"><span data-stu-id="f073f-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="f073f-132">La palabra clave TABLE, seguida del nombre de una tabla en el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="f073f-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="f073f-133">*alias secundario*</span><span class="sxs-lookup"><span data-stu-id="f073f-133">*child-alias*</span></span>

  - <span data-ttu-id="f073f-134">Alias que hace referencia al objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="f073f-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="f073f-135">*columna primaria*</span><span class="sxs-lookup"><span data-stu-id="f073f-135">*parent-column*</span></span>

  - <span data-ttu-id="f073f-136">Una columna en el **conjunto de registros** devuelto por la *comando primario.*</span><span class="sxs-lookup"><span data-stu-id="f073f-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="f073f-137">*columna secundaria*</span><span class="sxs-lookup"><span data-stu-id="f073f-137">*child-column*</span></span>

  - <span data-ttu-id="f073f-138">Columna del objeto **Recordset** que devuelve el *comando secundario*.</span><span class="sxs-lookup"><span data-stu-id="f073f-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="f073f-139">*número de parámetros*</span><span class="sxs-lookup"><span data-stu-id="f073f-139">*param-number*</span></span>

  - <span data-ttu-id="f073f-140">Vea [Funcionamiento de los comandos parametrizados](operation-of-parameterized-commands.md).</span><span class="sxs-lookup"><span data-stu-id="f073f-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="f073f-141">*alias de capítulo*</span><span class="sxs-lookup"><span data-stu-id="f073f-141">*chapter-alias*</span></span>

  - <span data-ttu-id="f073f-142">Alias que hace referencia a la columna de capítulo anexada a la columna primaria.</span><span class="sxs-lookup"><span data-stu-id="f073f-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="f073f-143">La cláusula _"columna a primaria TO columna a secundaria"_ es en realidad una lista, donde cada relación definida viene separada por una coma.</span><span class="sxs-lookup"><span data-stu-id="f073f-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="f073f-144">[!NOTA] La cláusula situada detrás de la palabra clave APPEND es en realidad una lista donde cada cláusula viene separada por una coma y define otra columna que se va a anexar a la columna primaria.</span><span class="sxs-lookup"><span data-stu-id="f073f-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="f073f-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f073f-145">Remarks</span></span>

<span data-ttu-id="f073f-p105">Al crear comandos de proveedor a partir de datos proporcionados por el usuario como parte de un comando SHAPE, este comando tratará el comando de proveedor proporcionado por el usuario como una cadena opaca y lo pasará fielmente al proveedor. Por ejemplo en el siguiente comando SHAPE,</span><span class="sxs-lookup"><span data-stu-id="f073f-p105">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider. For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="f073f-148">SHAPE ejecutará dos comandos: seleccione \* from t1 y (seleccione \* from t2 RELATE k1 TO k2).</span><span class="sxs-lookup"><span data-stu-id="f073f-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="f073f-149">Si el usuario proporciona un comando compuesto formado por varios comandos de proveedor separados por signos de punto de coma, SHAPE no es capaz de discernir la diferencia.</span><span class="sxs-lookup"><span data-stu-id="f073f-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="f073f-150">Por lo tanto, en el siguiente comando SHAPE,</span><span class="sxs-lookup"><span data-stu-id="f073f-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="f073f-151">SHAPE ejecuta select \* from t1; DROP table t1 y (seleccione \* from t2 RELATE k1 TO k2), sin darse cuenta de que drop table t1 es un independiente y en este comando de proveedor caso, peligroso.</span><span class="sxs-lookup"><span data-stu-id="f073f-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="f073f-152">Las aplicaciones siempre deben validar los datos proporcionados por el usuario para evitar que se produzcan esos posibles ataques de piratas informáticos.</span><span class="sxs-lookup"><span data-stu-id="f073f-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>
