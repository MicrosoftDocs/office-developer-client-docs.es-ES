---
title: Tipos de datos SQL (referencia de la base de datos de escritorio de Access)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb72a0090550692e7cf5028a6a58a078fc5d9d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308585"
---
# <a name="sql-data-types"></a><span data-ttu-id="f9c9f-102">Tipos de datos SQL</span><span class="sxs-lookup"><span data-stu-id="f9c9f-102">SQL data types</span></span>

<span data-ttu-id="f9c9f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9c9f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9c9f-104">Los tipos de datos SQL del motor de base de datos de Microsoft Access están formados por 13 tipos de datos principales definidos por el motor de base de datos Microsoft Jet y varios sinónimos válidos reconocidos para estos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft® Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="f9c9f-105">En la tabla siguiente se enumeran los tipos de datos principales.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-105">The following table lists the primary data types.</span></span> <span data-ttu-id="f9c9f-106">Los sinónimos se identifican en [Palabras reservadas SQL del motor de base de datos de Microsoft Access](sql-reserved-words.md).</span><span class="sxs-lookup"><span data-stu-id="f9c9f-106">The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9c9f-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f9c9f-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="f9c9f-108">Tamaño de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="f9c9f-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="f9c9f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9c9f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9c9f-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="f9c9f-110">Binary</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-111">1 byte por carácter</span><span class="sxs-lookup"><span data-stu-id="f9c9f-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-p102">En un campo de este tipo se puede almacenar cualquier tipo de datos. No se realiza ninguna conversión de los datos (por ejemplo, a texto). La forma de introducir los datos en un campo binario define cómo se mostrarán como resultado.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-p102">Any type of data may be stored in a field of this type. No translation of the data (for example, to text) is made. How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c9f-115">BIT</span><span class="sxs-lookup"><span data-stu-id="f9c9f-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-116">1 byte</span><span class="sxs-lookup"><span data-stu-id="f9c9f-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-117">Los valores y los campos Sí y No solo pueden contener uno de los dos valores.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c9f-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="f9c9f-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-119">1 byte</span><span class="sxs-lookup"><span data-stu-id="f9c9f-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-120">Un valor entero entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c9f-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="f9c9f-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-122">8 bytes</span><span class="sxs-lookup"><span data-stu-id="f9c9f-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-123">Entero con ajuste de escala entre – 922.337.203.685.477,5808 y 922.337.203.685.477,5807.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c9f-124">DATETIME (vea DOUBLE)</span><span class="sxs-lookup"><span data-stu-id="f9c9f-124">DATETIME
(See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-125">8 bytes</span><span class="sxs-lookup"><span data-stu-id="f9c9f-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-126">Un valor de fecha u hora entre los años 100 y 9999.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c9f-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="f9c9f-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-128">128 bits</span><span class="sxs-lookup"><span data-stu-id="f9c9f-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-129">Un número de identificación único que se usa con llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c9f-130">REAL</span><span class="sxs-lookup"><span data-stu-id="f9c9f-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-131">4 bytes</span><span class="sxs-lookup"><span data-stu-id="f9c9f-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-132">Un valor de coma flotante de precisión sencilla entre -3,402823E38 y -1,401298E-45 para los valores negativos, y entre 1,401298E-45 y 3,402823E38 para los valores positivos y 0.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c9f-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f9c9f-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-134">8 bytes</span><span class="sxs-lookup"><span data-stu-id="f9c9f-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-135">Un valor de coma flotante de precisión doble entre -1,79769313486232E308 y -4,94065645841247E-324 para los valores negativos, y entre 4,94065645841247E-324 y 1,79769313486232E308 para los valores positivos y 0.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c9f-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="f9c9f-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-137">2 bytes</span><span class="sxs-lookup"><span data-stu-id="f9c9f-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-p103">Entero corto entre – 32.768 y 32.767. (Vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="f9c9f-p103">A short integer between – 32,768 and 32,767. (See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c9f-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="f9c9f-140">Integer</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-141">4 bytes</span><span class="sxs-lookup"><span data-stu-id="f9c9f-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-p104">Entero largo entre – 2.147.483.648 y 2.147.483.647. (Vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="f9c9f-p104">A long integer between – 2,147,483,648 and 2,147,483,647. (See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c9f-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="f9c9f-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-145">17 bytes</span><span class="sxs-lookup"><span data-stu-id="f9c9f-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-p105">Un tipo de datos numérico exacto que contiene valores desde 1028-1 hasta -1028-1. Se puede definir la precisión (1-28) y la escala (0-precisión definida). La precisión y escala predeterminadas son 18 y 0, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-p105">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1. You can define both precision (1 - 28) and scale (0 - defined precision). The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c9f-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="f9c9f-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-150">2 bytes por carácter (vea la nota)</span><span class="sxs-lookup"><span data-stu-id="f9c9f-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-151">De cero a un máximo de 2,14 gigabytes.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c9f-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="f9c9f-152">Image</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-153">Según sea necesario</span><span class="sxs-lookup"><span data-stu-id="f9c9f-153">As required</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-p106">De cero a un máximo de 2,14 gigabytes. Se usa para objetos OLE.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-p106">Zero to a maximum of 2.14 gigabytes. Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c9f-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="f9c9f-156">Character</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-157">2 bytes por carácter (vea las Notas)</span><span class="sxs-lookup"><span data-stu-id="f9c9f-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="f9c9f-158">De cero a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - <span data-ttu-id="f9c9f-p107">El valor de inicialización y el incremento se pueden modificar mediante una [instrucción ALTER TABLE](alter-table-statement-microsoft-access-sql.md). Las filas nuevas insertadas en la tabla tendrán valores, basados en los nuevos valores de inicialización e incremento, que se generan automáticamente para la columna. Si los nuevos valores de inicialización e incremento pueden proporcionar valores que coinciden con los valores generados en función de los valores de inicialización e incremento anteriores, se generarán valores duplicados. Si la columna es una clave principal, la inserción de nuevas filas puede producir errores al generarse valores duplicados.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-p107">Both the seed and the increment can be modified using an [ALTER TABLE statement](alter-table-statement-microsoft-access-sql.md). New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column. If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated. If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span>
> - <span data-ttu-id="f9c9f-p108">Para buscar el último valor que se usó para una columna de incremento automático, puede utilizar la siguiente instrucción: SELECT @@IDENTITY. No puede especificar el nombre de una tabla. El valor devuelto pertenece a la última tabla, que contenga una columna de incremento automático, que se actualizó.</span><span class="sxs-lookup"><span data-stu-id="f9c9f-p108">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY. You cannot specify a table name. The value returned is from the last table, containing an auto-increment column, that was updated.</span></span>
