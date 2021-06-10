---
title: Proveedor de Microsoft OLE DB para Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9b506f40039ff91a6b1985606322fd86a9e7c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288935"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="e93cd-102">Proveedor de Microsoft OLE DB para Oracle</span><span class="sxs-lookup"><span data-stu-id="e93cd-102">Microsoft OLE DB Provider for Oracle</span></span>

<span data-ttu-id="e93cd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e93cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e93cd-104">El Proveedor de Microsoft OLE DB para Oracle permite que ADO obtenga acceso a bases de datos de Oracle.</span><span class="sxs-lookup"><span data-stu-id="e93cd-104">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="e93cd-105">Parámetros de la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="e93cd-105">Connection String Parameters</span></span>

<span data-ttu-id="e93cd-106">Para conectar con este proveedor, establezca el argumento *Provider* de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="e93cd-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAORA 
```

<span data-ttu-id="e93cd-107">La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.</span><span class="sxs-lookup"><span data-stu-id="e93cd-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

<span data-ttu-id="e93cd-p101">Si se ejecuta una consulta conjunta con un conjunto de claves o cursor dinámico en una base de datos de Oracle, se produce un error. Oracle solamente admite un cursor estático de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e93cd-p101">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs. Oracle only supports a static read-only cursor.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="e93cd-110">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="e93cd-110">Typical Connection String</span></span>

<span data-ttu-id="e93cd-111">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="e93cd-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

<span data-ttu-id="e93cd-112">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="e93cd-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e93cd-113">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="e93cd-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="e93cd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e93cd-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e93cd-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-116">Especifica el Proveedor OLE DB para Oracle.</span><span class="sxs-lookup"><span data-stu-id="e93cd-116">Specifies the OLE DB Provider for Oracle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e93cd-117"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-117"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-118">Especifica el nombre de un servidor.</span><span class="sxs-lookup"><span data-stu-id="e93cd-118">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e93cd-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-120">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="e93cd-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e93cd-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-122">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="e93cd-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="e93cd-123">Parámetros de conexión específicos del proveedor</span><span class="sxs-lookup"><span data-stu-id="e93cd-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="e93cd-p102">El proveedor admite varios parámetros de conexión específicos del proveedor además de los definidos por ADO. Al igual que las propiedades de conexión ADO, estas propiedades específicas del proveedor se pueden establecer mediante la colección [Properties](properties-collection-ado.md) de un objeto [Connection](connection-object-ado.md) o como parte de **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="e93cd-p102">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or as part of the **ConnectionString**.</span></span>

<span data-ttu-id="e93cd-p103">Estos parámetros se describen en profundidad en la Referencia del programador de OLE DB. (El [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md) proporciona una referencia cruzada entre estos nombres de parámetro y las propiedades de OLE DB correspondientes.)</span><span class="sxs-lookup"><span data-stu-id="e93cd-p103">These parameters are fully described in the OLE DB Programmer's Reference. (The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e93cd-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e93cd-128">Parameter</span></span></p></th>
<th><p><span data-ttu-id="e93cd-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e93cd-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e93cd-130"><strong>Window Handle</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-130"><strong>Window Handle</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-131">Indica el controlador de ventana que se utilizará para solicitar información adicional.</span><span class="sxs-lookup"><span data-stu-id="e93cd-131">Indicates the window handle to use to prompt for additional information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e93cd-132"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-132"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-p104">Indica un número exclusivo de 32 bits (por ejemplo, 1033) que especifica las preferencias relacionadas con el idioma del usuario. Estas preferencias indican el formato de las fechas y las horas, el modo en que los elementos se ordenan alfabéticamente y en que se comparan las cadenas, etc.</span><span class="sxs-lookup"><span data-stu-id="e93cd-p104">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e93cd-135"><strong>OLE DB Services</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-135"><strong>OLE DB Services</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-136">Indica una máscara de bits que especifica los servicios OLE DB que se van a habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="e93cd-136">Indicates a bitmask that specifies OLE DB services to enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e93cd-137"><strong>Prompt</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-137"><strong>Prompt</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-138">Indica si es necesario preguntar al usuario mientras se está estableciendo una conexión.</span><span class="sxs-lookup"><span data-stu-id="e93cd-138">Indicates whether to prompt the user while a connection is being established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e93cd-139"><strong>Extended Properties</strong></span><span class="sxs-lookup"><span data-stu-id="e93cd-139"><strong>Extended Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="e93cd-p105">Una cadena que contiene información de conexión ampliada específica del proveedor. Utilice esta propiedad únicamente para la información de conexión específica del proveedor que no se pueda describir por medio del mecanismo de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e93cd-p105">A string containing provider-specific, extended connection information. Use this property only for provider-specific connection information that cannot be described through the property mechanism.</span></span></p></td>
</tr>
</tbody>
</table>

