---
title: Utilizar ADO con lenguajes de secuencias de comandos
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00854a56428a99a4d033f7959690836f88912c77
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944805"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="e17d1-102">Utilizar ADO con lenguajes de scripting</span><span class="sxs-lookup"><span data-stu-id="e17d1-102">Using ADO with scripting languages</span></span>


<span data-ttu-id="e17d1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e17d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e17d1-104">Dentro de un entorno de secuencias de comandos, ADO permite exponer datos mediante secuencias de comandos de servidor.</span><span class="sxs-lookup"><span data-stu-id="e17d1-104">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="e17d1-105">En este escenario, ADO, el proveedor OLE DB subyacente que utiliza y todos los componentes necesarios para hacer referencia a un almacén de datos determinada están instalados en un servidor que ejecuta Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="e17d1-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="e17d1-106">Uso de páginas Active Server (ASP), ADO es un componente que se hace referencia en una secuencia de comandos que puede generar HTML, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e17d1-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="e17d1-107">Este contenido HTML se puede pasar a través de HTTP en un explorador web del cliente.</span><span class="sxs-lookup"><span data-stu-id="e17d1-107">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="e17d1-108">Mediante el uso de secuencias de comandos, la página Web puede devolver acciones a la secuencia de comandos del lado del servidor, lo que le permite actualizar, recorrer o ver datos específicos.</span><span class="sxs-lookup"><span data-stu-id="e17d1-108">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="e17d1-109">Orígenes de datos ODBC</span><span class="sxs-lookup"><span data-stu-id="e17d1-109">ODBC Data Sources</span></span>

<span data-ttu-id="e17d1-p102">Una diferencia importante entre código de ADO que consta de secuencias de comandos y código de ADO que no consta de secuencias de comandos es el origen de datos ODBC, en caso de que se utilice. Para las aplicaciones que no sean secuencias de comandos, se puede crear un DSN de usuario en el Administrador de orígenes de datos ODBC. Para las secuencias de comandos que se ejecutan en IIS, debe crear un DSN de sistema; en caso contrario, las secuencias de comandos no reconocerán el origen de datos creado. Esto se aplica a cualquier aplicación de secuencias de comandos de ADO que utilice el proveedor de Microsoft OLE DB para ODBC a través de Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="e17d1-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="e17d1-114">Hacer referencia a la biblioteca de ADO</span><span class="sxs-lookup"><span data-stu-id="e17d1-114">Referencing the ADO Library</span></span>

<span data-ttu-id="e17d1-115">No está disponible con los lenguajes de secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="e17d1-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="e17d1-116">Controlar eventos</span><span class="sxs-lookup"><span data-stu-id="e17d1-116">Handling events</span></span>

<span data-ttu-id="e17d1-117">No está disponible con los lenguajes de secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="e17d1-117">N/A with scripting languages.</span></span>

<span data-ttu-id="e17d1-118">Los temas siguientes contienen información más específica sobre la utilización de ADO con los lenguajes de secuencias de comandos:</span><span class="sxs-lookup"><span data-stu-id="e17d1-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

- [<span data-ttu-id="e17d1-119">Programación de ADO con JScript</span><span class="sxs-lookup"><span data-stu-id="e17d1-119">JScript ADO Programming</span></span>](jscript-ado-programming.md)

- [<span data-ttu-id="e17d1-120">Programación ADO en VBScript</span><span class="sxs-lookup"><span data-stu-id="e17d1-120">VBScript ADO Programming</span></span>](vbscript-ado-programming.md)