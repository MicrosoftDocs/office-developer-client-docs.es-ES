---
title: Introducción al archivo de personalización
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314073"
---
# <a name="understanding-the-customization-file"></a><span data-ttu-id="d936b-102">Introducción al archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="d936b-102">Understanding the Customization File</span></span>


<span data-ttu-id="d936b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d936b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d936b-104">Cada encabezado de sección del archivo de personalización consta de corchetes ( **\[\]** ) que contienen un tipo y parámetro.</span><span class="sxs-lookup"><span data-stu-id="d936b-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="d936b-105">Los cuatro tipos de sección vienen indicados por las cadenas literales **connect**, **sql**, **userlist** o **logs**.</span><span class="sxs-lookup"><span data-stu-id="d936b-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="d936b-106">El parámetro es la cadena literal, el valor predeterminado, un identificador especificado por el usuario o nada.</span><span class="sxs-lookup"><span data-stu-id="d936b-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="d936b-107">Por lo tanto, cada sección viene marcada con uno de los encabezados siguientes:</span><span class="sxs-lookup"><span data-stu-id="d936b-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="d936b-108">Los encabezados de sección constan de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="d936b-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d936b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d936b-109">Part</span></span></p></th>
<th><p><span data-ttu-id="d936b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d936b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d936b-111"><strong>conectar</strong></span><span class="sxs-lookup"><span data-stu-id="d936b-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="d936b-112">Cadena literal que modifica una cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="d936b-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d936b-113"><strong>sql</strong></span><span class="sxs-lookup"><span data-stu-id="d936b-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="d936b-114">Cadena literal que modifica una cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="d936b-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d936b-115"><strong>userlist</strong></span><span class="sxs-lookup"><span data-stu-id="d936b-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="d936b-116">Cadena literal que modifica los derechos de acceso de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="d936b-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d936b-117"><strong>registros</strong></span><span class="sxs-lookup"><span data-stu-id="d936b-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="d936b-118">Cadena literal que especifica un archivo de registro donde se registran los errores operativos.</span><span class="sxs-lookup"><span data-stu-id="d936b-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d936b-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="d936b-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="d936b-120">Cadena literal que se utiliza si no se ha especificado o no se encuentra ningún identificador.</span><span class="sxs-lookup"><span data-stu-id="d936b-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d936b-121"><em>identificador</em></span><span class="sxs-lookup"><span data-stu-id="d936b-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="d936b-122">Cadena que corresponde a una cadena en la cadena de <strong>conexión</strong> o de <strong>comandos</strong>.</span><span class="sxs-lookup"><span data-stu-id="d936b-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="d936b-123">Utilice esta sección si el encabezado de sección contiene <strong>connect</strong> y se encuentra la cadena de identificador en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="d936b-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="d936b-124">Utilice esta sección si el encabezado de sección contiene <strong>sql</strong> y se encuentra la cadena de identificador en la cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="d936b-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="d936b-125">Utilice esta sección si el encabezado de sección contiene <strong>userlist</strong> y la cadena de identificador coincide con un identificador de la sección <strong>connect</strong>.</span><span class="sxs-lookup"><span data-stu-id="d936b-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d936b-p102">**DataFactory** llama al controlador, pasando parámetros de cliente. El controlador busca cadenas completas en los parámetros de cliente que coincidan con los identificadores en los correspondientes encabezados de sección. Si se encuentra una coincidencia, se aplica el contenido de esa sección al parámetro de cliente.</span><span class="sxs-lookup"><span data-stu-id="d936b-p102">The **DataFactory** calls the handler, passing client parameters. The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers. If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="d936b-129">Se utiliza una sección concreta en las circunstancias siguientes:</span><span class="sxs-lookup"><span data-stu-id="d936b-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="d936b-130">Se **usa** una sección connect si la parte de valor de la palabra clave de cadena connect del cliente, "\**Data Source=\*\*\*value",* coincide con un identificador **de** sección connect *.*</span><span class="sxs-lookup"><span data-stu-id="d936b-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="d936b-131">Se utiliza una sección **sql** si la cadena de comandos del cliente contiene una cadena que coincide con un identificador de la sección **sql**.</span><span class="sxs-lookup"><span data-stu-id="d936b-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="d936b-132">Se utiliza una sección **connect** o **sql** con un parámetro predeterminado si no hay ningún identificador coincidente.</span><span class="sxs-lookup"><span data-stu-id="d936b-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="d936b-p103">Se utiliza una sección **userlist** si el identificador de la sección **userlist** coincide con un identificador de la sección **connect**. Si hay una coincidencia, se aplica el contenido de la sección **userlist** a la conexión que rige la sección **connect**.</span><span class="sxs-lookup"><span data-stu-id="d936b-p103">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier. If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="d936b-135">Si la cadena en una cadena de conexión o de comandos no coincide con ningún identificador del encabezado de sección **connect** o **sql**, y si no hay ningún encabezado de sección **connect** o **sql** con un parámetro predeterminado, se utilizará la cadena de cliente sin modificación alguna.</span><span class="sxs-lookup"><span data-stu-id="d936b-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="d936b-136">Se utiliza la sección **logs** cada vez que se encuentra operativo el objeto **DataFactory**.</span><span class="sxs-lookup"><span data-stu-id="d936b-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

