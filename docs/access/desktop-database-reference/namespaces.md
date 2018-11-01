---
title: Espacios de nombres (referencia de escritorio de la base de datos de Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef37f04ec6824cedf773cb72751b2364d2b3edf8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876564"
---
# <a name="namespaces"></a><span data-ttu-id="fd0e4-102">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="fd0e4-102">Namespaces</span></span>


<span data-ttu-id="fd0e4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd0e4-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="namespaces"></a><span data-ttu-id="fd0e4-104">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="fd0e4-104">Namespaces</span></span>

<span data-ttu-id="fd0e4-105">El formato XML persistente en ADO utiliza los cuatro espacios de nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd0e4-105">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd0e4-106">Prefijo</span><span class="sxs-lookup"><span data-stu-id="fd0e4-106">Prefix</span></span></p></th>
<th><p><span data-ttu-id="fd0e4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd0e4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd0e4-108">s</span><span class="sxs-lookup"><span data-stu-id="fd0e4-108">s</span></span></p></td>
<td><p><span data-ttu-id="fd0e4-109">Hace referencia a la &quot;datos XML&quot; espacio de nombres que contiene los elementos y atributos que definen el esquema del <strong>conjunto de registros</strong>actual.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-109">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0e4-110">dt</span><span class="sxs-lookup"><span data-stu-id="fd0e4-110">dt</span></span></p></td>
<td><p><span data-ttu-id="fd0e4-111">Hace referencia a la especificación de definiciones de tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-111">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd0e4-112">rs</span><span class="sxs-lookup"><span data-stu-id="fd0e4-112">rs</span></span></p></td>
<td><p><span data-ttu-id="fd0e4-113">Hace referencia al espacio de nombres que contiene elementos y atributos específicos de propiedades y atributos del <strong>conjunto de registros</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-113">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0e4-114">z</span><span class="sxs-lookup"><span data-stu-id="fd0e4-114">z</span></span></p></td>
<td><p><span data-ttu-id="fd0e4-115">Hace referencia al esquema del conjunto de filas activo.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-115">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fd0e4-p101">Un cliente no debe agregar sus propias etiquetas a estos espacios de nombres, según se define en las especificaciones. Por ejemplo, un cliente no debe definir un espacio de nombres como "urn:schemas-microsoft-com:rowset" y luego escribir algo como "rs:MiEtiqueta". Para obtener más información acerca de espacios de nombres, vea [Espacios de nombres XML](https://www.w3.org/tr/xml-names/).</span><span class="sxs-lookup"><span data-stu-id="fd0e4-p101">A client should not add its own tags to these namespaces, as defined by the specification. For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag." To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>


> [!NOTE]
> <P><span data-ttu-id="fd0e4-119">[!NOTA] El identificador para la etiqueta del esquema debe ser "RowsetSchema" y el espacio de nombres utilizado para hacer referencia al esquema del conjunto de filas activo debe apuntar a "#RowsetSchema".</span><span class="sxs-lookup"><span data-stu-id="fd0e4-119">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span></P>



<span data-ttu-id="fd0e4-120">Tenga en cuenta que el prefijo del espacio de nombres, que parte a la derecha de la coma y a la izquierda del signo igual, es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-120">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="fd0e4-p102">El usuario puede definirlo de modo que sea cualquier nombre, siempre que este nombre se utilice incoherentemente en todo el documento XML. ADO siempre escribe "s" "rs" "dt" y "z", pero estos nombres de prefijos no se codifican de forma rígida en el componente de carga.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-p102">The user can define this to be any name as long as this name is consistently used throughout the XML document. ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>

## <a name="namespaces"></a><span data-ttu-id="fd0e4-123">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="fd0e4-123">Namespaces</span></span>

<span data-ttu-id="fd0e4-124">El formato XML persistente en ADO utiliza los cuatro espacios de nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd0e4-124">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd0e4-125">Prefijo</span><span class="sxs-lookup"><span data-stu-id="fd0e4-125">Prefix</span></span></p></th>
<th><p><span data-ttu-id="fd0e4-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd0e4-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd0e4-127">s</span><span class="sxs-lookup"><span data-stu-id="fd0e4-127">s</span></span></p></td>
<td><p><span data-ttu-id="fd0e4-128">Hace referencia a la &quot;datos XML&quot; espacio de nombres que contiene los elementos y atributos que definen el esquema del <strong>conjunto de registros</strong>actual.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-128">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0e4-129">dt</span><span class="sxs-lookup"><span data-stu-id="fd0e4-129">dt</span></span></p></td>
<td><p><span data-ttu-id="fd0e4-130">Hace referencia a la especificación de definiciones de tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-130">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd0e4-131">rs</span><span class="sxs-lookup"><span data-stu-id="fd0e4-131">rs</span></span></p></td>
<td><p><span data-ttu-id="fd0e4-132">Hace referencia al espacio de nombres que contiene elementos y atributos específicos de propiedades y atributos del <strong>conjunto de registros</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-132">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0e4-133">z</span><span class="sxs-lookup"><span data-stu-id="fd0e4-133">z</span></span></p></td>
<td><p><span data-ttu-id="fd0e4-134">Hace referencia al esquema del conjunto de filas activo.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-134">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fd0e4-p103">Un cliente no debe agregar sus propias etiquetas a estos espacios de nombres, según se define en las especificaciones. Por ejemplo, un cliente no debe definir un espacio de nombres como "urn:schemas-microsoft-com:rowset" y luego escribir algo como "rs:MiEtiqueta". Para obtener más información acerca de espacios de nombres, vea [Espacios de nombres XML](https://www.w3.org/tr/xml-names/).</span><span class="sxs-lookup"><span data-stu-id="fd0e4-p103">A client should not add its own tags to these namespaces, as defined by the specification. For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag." To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>


> [!NOTE]
> <P><span data-ttu-id="fd0e4-138">[!NOTA] El identificador para la etiqueta del esquema debe ser "RowsetSchema" y el espacio de nombres utilizado para hacer referencia al esquema del conjunto de filas activo debe apuntar a "#RowsetSchema".</span><span class="sxs-lookup"><span data-stu-id="fd0e4-138">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span></P>



<span data-ttu-id="fd0e4-139">Tenga en cuenta que el prefijo del espacio de nombres, que parte a la derecha de la coma y a la izquierda del signo igual, es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-139">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="fd0e4-p104">El usuario puede definirlo de modo que sea cualquier nombre, siempre que este nombre se utilice incoherentemente en todo el documento XML. ADO siempre escribe "s" "rs" "dt" y "z", pero estos nombres de prefijos no se codifican de forma rígida en el componente de carga.</span><span class="sxs-lookup"><span data-stu-id="fd0e4-p104">The user can define this to be any name as long as this name is consistently used throughout the XML document. ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>

