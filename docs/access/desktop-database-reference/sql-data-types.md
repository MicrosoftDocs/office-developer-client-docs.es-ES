---
title: Tipos de datos de SQL (referencia de escritorio de la base de datos de Access)
TOCTitle: SQL Data Types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fd49861af896ae1c2d55a80665f119662c0baf53
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880400"
---
# <a name="sql-data-types"></a><span data-ttu-id="3066c-102">Tipos de datos SQL</span><span class="sxs-lookup"><span data-stu-id="3066c-102">SQL Data Types</span></span>


<span data-ttu-id="3066c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3066c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3066c-104">Los tipos de datos SQL del motor de base de datos de Microsoft Access están formados por 13 tipos de datos principales definidos por el motor de base de datos Microsoft® Jet y varios sinónimos válidos reconocidos para estos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="3066c-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft® Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="3066c-p101">En la siguiente tabla, se enumeran los tipos de datos principales. Los sinónimos se identifican en [Palabras reservadas SQL del motor de base de datos de Microsoft Access](sql-reserved-words.md).</span><span class="sxs-lookup"><span data-stu-id="3066c-p101">The following table lists the primary data types. The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3066c-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3066c-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="3066c-108">Tamaño de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="3066c-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="3066c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3066c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3066c-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="3066c-110">BINARY</span></span></p></td>
<td><p><span data-ttu-id="3066c-111">1 byte por carácter</span><span class="sxs-lookup"><span data-stu-id="3066c-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="3066c-p102">En este tipo de campo se puede almacenar cualquier tipo de datos. No se realiza ninguna conversión de los datos (por ejemplo, a texto). La forma en que se especifiquen los datos en un campo binario determina cómo aparecerán en los resultados.</span><span class="sxs-lookup"><span data-stu-id="3066c-p102">Any type of data may be stored in a field of this type. No translation of the data (for example, to text) is made. How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3066c-115">BIT</span><span class="sxs-lookup"><span data-stu-id="3066c-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="3066c-116">1 byte</span><span class="sxs-lookup"><span data-stu-id="3066c-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="3066c-117">Valores Sí y No, y campos que contienen uno de dos valores posibles.</span><span class="sxs-lookup"><span data-stu-id="3066c-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3066c-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="3066c-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="3066c-119">1 byte</span><span class="sxs-lookup"><span data-stu-id="3066c-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="3066c-120">Valor entero entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="3066c-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3066c-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="3066c-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="3066c-122">8 bytes</span><span class="sxs-lookup"><span data-stu-id="3066c-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="3066c-123">Entero con ajuste de escala entre – 922.337.203.685.477,5808 y 922.337.203.685.477,5807.</span><span class="sxs-lookup"><span data-stu-id="3066c-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3066c-124">DATETIME (vea DOUBLE)</span><span class="sxs-lookup"><span data-stu-id="3066c-124">DATETIME (See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="3066c-125">8 bytes</span><span class="sxs-lookup"><span data-stu-id="3066c-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="3066c-126">Valor de fecha u hora entre los años 100 y 9999.</span><span class="sxs-lookup"><span data-stu-id="3066c-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3066c-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="3066c-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="3066c-128">128 bits</span><span class="sxs-lookup"><span data-stu-id="3066c-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="3066c-129">Número de identificación único que se usa con llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="3066c-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3066c-130">REAL</span><span class="sxs-lookup"><span data-stu-id="3066c-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="3066c-131">4 bytes</span><span class="sxs-lookup"><span data-stu-id="3066c-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="3066c-132">Valor de coma flotante de precisión única con un intervalo desde – 3,402823E38 hasta – 1,401298E-45 para valores negativos; desde 1,401298E-45 hasta 3,402823E38 para valores positivos; y 0.</span><span class="sxs-lookup"><span data-stu-id="3066c-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3066c-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3066c-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="3066c-134">8 bytes</span><span class="sxs-lookup"><span data-stu-id="3066c-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="3066c-135">Valor de coma flotante de precisión doble con un intervalo desde – 1,79769313486232E308 hasta – 4,94065645841247E-324 para valores negativos; desde 4,94065645841247E-324 hasta 1,79769313486232E308 para valores positivos; y 0.</span><span class="sxs-lookup"><span data-stu-id="3066c-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3066c-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="3066c-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="3066c-137">2 bytes</span><span class="sxs-lookup"><span data-stu-id="3066c-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="3066c-p103">Entero corto entre – 32.768 y 32.767. (Vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="3066c-p103">A short integer between – 32,768 and 32,767. (See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3066c-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="3066c-140">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="3066c-141">4 bytes</span><span class="sxs-lookup"><span data-stu-id="3066c-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="3066c-p104">Entero largo entre – 2.147.483.648 y 2.147.483.647. (Vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="3066c-p104">A long integer between – 2,147,483,648 and 2,147,483,647. (See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3066c-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="3066c-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="3066c-145">17 bytes</span><span class="sxs-lookup"><span data-stu-id="3066c-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="3066c-p105">Tipo de datos numérico exacto que contiene valores desde 1028 - 1 hasta - 1028 - 1. Puede definir la precisión (1 - 28) y la escala (0 - precisión definida). La precisión y escala predeterminadas son 18 y 0, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3066c-p105">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1. You can define both precision (1 - 28) and scale (0 - defined precision). The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3066c-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="3066c-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="3066c-150">2 bytes por carácter (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="3066c-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="3066c-151">De cero a un máximo de 2,14 gigabytes.</span><span class="sxs-lookup"><span data-stu-id="3066c-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3066c-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="3066c-152">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="3066c-153">Según corresponda</span><span class="sxs-lookup"><span data-stu-id="3066c-153">As required</span></span></p></td>
<td><p><span data-ttu-id="3066c-p106">De cero a un máximo de 2,14 gigabytes. Se usa para objetos OLE.</span><span class="sxs-lookup"><span data-stu-id="3066c-p106">Zero to a maximum of 2.14 gigabytes. Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3066c-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="3066c-156">CHARACTER</span></span></p></td>
<td><p><span data-ttu-id="3066c-157">2 bytes por carácter (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="3066c-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="3066c-158">De cero a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3066c-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="3066c-p107">El valor de inicialización y el incremento se pueden modificar mediante una <A href="alter-table-statement-microsoft-access-sql.md">instrucción ALTER TABLE</A>. Las filas nuevas insertadas en la tabla tendrán valores, basados en los nuevos valores de inicialización e incremento, que se generan automáticamente para la columna. Si los nuevos valores de inicialización e incremento pueden proporcionar valores que coinciden con los valores generados en función de los valores de inicialización e incremento anteriores, se generarán valores duplicados. Si la columna es una clave principal, la inserción de nuevas filas puede producir errores al generarse valores duplicados.</span><span class="sxs-lookup"><span data-stu-id="3066c-p107">Both the seed and the increment can be modified using an <A href="alter-table-statement-microsoft-access-sql.md">ALTER TABLE statement</A>. New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column. If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated. If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span></P>
> <LI>
> <P><span data-ttu-id="3066c-p108">Para buscar el último valor que se usó para una columna de incremento automático, puede utilizar la siguiente instrucción: SELECT @@IDENTITY. No puede especificar el nombre de una tabla. El valor devuelto pertenece a la última tabla, que contenga una columna de incremento automático, que se actualizó.</span><span class="sxs-lookup"><span data-stu-id="3066c-p108">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY. You cannot specify a table name. The value returned is from the last table, containing an auto-increment column, that was updated.</span></span></P></LI></UL>


