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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721888"
---
# <a name="understanding-the-customization-file"></a><span data-ttu-id="c9d76-102">Introducción al archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="c9d76-102">Understanding the Customization File</span></span>


<span data-ttu-id="c9d76-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9d76-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9d76-104">Cada encabezado de sección en el archivo de personalización consta de corchetes (**\[**) que contiene un tipo y un parámetro.</span><span class="sxs-lookup"><span data-stu-id="c9d76-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="c9d76-105">Los cuatro tipos de sección vienen indicados por las cadenas literales **connect**, **sql**, **userlist** o **logs**.</span><span class="sxs-lookup"><span data-stu-id="c9d76-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="c9d76-106">El parámetro es la cadena literal, el valor predeterminado, un identificador especificado por el usuario o nada.</span><span class="sxs-lookup"><span data-stu-id="c9d76-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="c9d76-107">Por lo tanto, cada sección viene marcada con uno de los encabezados siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9d76-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="c9d76-108">Los encabezados de sección constan de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="c9d76-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9d76-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9d76-109">Part</span></span></p></th>
<th><p><span data-ttu-id="c9d76-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9d76-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9d76-111"><strong>connect</strong></span><span class="sxs-lookup"><span data-stu-id="c9d76-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="c9d76-112">Cadena literal que modifica una cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="c9d76-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9d76-113"><strong>sql</strong></span><span class="sxs-lookup"><span data-stu-id="c9d76-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="c9d76-114">Cadena literal que modifica una cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="c9d76-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9d76-115"><strong>userlist</strong></span><span class="sxs-lookup"><span data-stu-id="c9d76-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="c9d76-116">Cadena literal que modifica los derechos de acceso de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="c9d76-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9d76-117"><strong>logs</strong></span><span class="sxs-lookup"><span data-stu-id="c9d76-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="c9d76-118">Cadena literal que especifica un archivo de registro donde se registran los errores operativos.</span><span class="sxs-lookup"><span data-stu-id="c9d76-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9d76-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="c9d76-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="c9d76-120">Cadena literal que se utiliza si no se ha especificado o no se encuentra ningún identificador.</span><span class="sxs-lookup"><span data-stu-id="c9d76-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9d76-121"><em>identifier</em></span><span class="sxs-lookup"><span data-stu-id="c9d76-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="c9d76-122">Cadena que corresponde a una cadena en la cadena de <strong>conexión</strong> o de <strong>comandos</strong>.
</span><span class="sxs-lookup"><span data-stu-id="c9d76-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="c9d76-123">Utilice esta sección si el encabezado de sección contiene <strong>connect</strong> y se encuentra la cadena de identificador en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="c9d76-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="c9d76-124">Utilice esta sección si el encabezado de sección contiene <strong>sql</strong> y se encuentra la cadena de identificador en la cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="c9d76-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="c9d76-125">Utilice esta sección si el encabezado de sección contiene <strong>userlist</strong> y la cadena de identificador coincide con un identificador de la sección <strong>connect</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9d76-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c9d76-p102">**DataFactory** llama al controlador, pasando parámetros de cliente. El controlador busca cadenas completas en los parámetros de cliente que coincidan con los identificadores en los correspondientes encabezados de sección. Si se encuentra una coincidencia, se aplica el contenido de esa sección al parámetro de cliente.</span><span class="sxs-lookup"><span data-stu-id="c9d76-p102">The **DataFactory** calls the handler, passing client parameters. The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers. If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="c9d76-129">Se utiliza una sección concreta en las circunstancias siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9d76-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="c9d76-130">Se utiliza una sección **connect** si la parte de valor del cliente conectar palabras clave de cadena, "\**origen de datos = \*\*\* valor*", coincide con un identificador de sección **connect** *.*</span><span class="sxs-lookup"><span data-stu-id="c9d76-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="c9d76-131">Se utiliza una sección **sql** si la cadena de comandos del cliente contiene una cadena que coincide con un identificador de la sección **sql**.</span><span class="sxs-lookup"><span data-stu-id="c9d76-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="c9d76-132">Se utiliza una sección **connect** o **sql** con un parámetro predeterminado si no hay ningún identificador coincidente.</span><span class="sxs-lookup"><span data-stu-id="c9d76-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="c9d76-p103">Se utiliza una sección **userlist** si el identificador de la sección **userlist** coincide con un identificador de la sección **connect**. Si hay una coincidencia, se aplica el contenido de la sección **userlist** a la conexión que rige la sección **connect**.</span><span class="sxs-lookup"><span data-stu-id="c9d76-p103">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier. If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="c9d76-135">Si la cadena en una cadena de conexión o de comandos no coincide con ningún identificador del encabezado de sección **connect** o **sql**, y si no hay ningún encabezado de sección **connect** o **sql** con un parámetro predeterminado, se utilizará la cadena de cliente sin modificación alguna.</span><span class="sxs-lookup"><span data-stu-id="c9d76-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="c9d76-136">Se utiliza la sección **logs** cada vez que se encuentra operativo el objeto **DataFactory**.</span><span class="sxs-lookup"><span data-stu-id="c9d76-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

