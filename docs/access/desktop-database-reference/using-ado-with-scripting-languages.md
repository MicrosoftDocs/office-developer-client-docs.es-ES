---
title: Utilizar ADO con lenguajes de secuencias de comandos
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 196366987e89f52a3c498a769fa501a3faca9dae
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604438"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="3e72f-102">Utilizar ADO con lenguajes de secuencias de comandos</span><span class="sxs-lookup"><span data-stu-id="3e72f-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="3e72f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e72f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3e72f-104"><<<<<<< HEAD dentro de un entorno de secuencias de comandos, ADO permite exponer datos mediante secuencias de comandos de servidor.</span><span class="sxs-lookup"><span data-stu-id="3e72f-104"><<<<<<< HEAD Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="3e72f-105">En este escenario, ADO, el proveedor OLE DB subyacente que utiliza y todos los componentes necesarios para hacer referencia a un almacén de datos determinada están instalados en un servidor que ejecuta Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="3e72f-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="3e72f-106">Uso de páginas Active Server (ASP), ADO es un componente que se hace referencia en una secuencia de comandos que puede generar HTML, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3e72f-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="3e72f-107">Este contenido HTML se puede pasar a través de HTTP en un explorador Web del cliente.</span><span class="sxs-lookup"><span data-stu-id="3e72f-107">This HTML content can be passed via HTTP to a client Web browser.</span></span> <span data-ttu-id="3e72f-108">Mediante el uso de secuencias de comandos, la página Web puede devolver acciones a la secuencia de comandos del lado del servidor, lo que le permite actualizar, recorrer o ver datos específicos.</span><span class="sxs-lookup"><span data-stu-id="3e72f-108">Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
<span data-ttu-id="3e72f-109">=== Dentro de un entorno de secuencias de comandos, ADO permite exponer datos mediante secuencias de comandos de servidor.</span><span class="sxs-lookup"><span data-stu-id="3e72f-109">======= Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="3e72f-110">En este escenario, ADO, el proveedor OLE DB subyacente que utiliza y todos los componentes necesarios para hacer referencia a un almacén de datos determinada están instalados en un servidor que ejecuta Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="3e72f-110">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="3e72f-111">Uso de páginas Active Server (ASP), ADO es un componente que se hace referencia en una secuencia de comandos que puede generar HTML, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3e72f-111">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="3e72f-112">Este contenido HTML se puede pasar a través de HTTP en un explorador web del cliente.</span><span class="sxs-lookup"><span data-stu-id="3e72f-112">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="3e72f-113">Mediante el uso de secuencias de comandos, la página Web puede devolver acciones a la secuencia de comandos del lado del servidor, lo que le permite actualizar, recorrer o ver datos específicos.</span><span class="sxs-lookup"><span data-stu-id="3e72f-113">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
>>>>>>> <span data-ttu-id="3e72f-114">master</span><span class="sxs-lookup"><span data-stu-id="3e72f-114">master</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="3e72f-115">Orígenes de datos ODBC</span><span class="sxs-lookup"><span data-stu-id="3e72f-115">ODBC Data Sources</span></span>

<span data-ttu-id="3e72f-p102">Una diferencia importante entre código de ADO que consta de secuencias de comandos y código de ADO que no consta de secuencias de comandos es el origen de datos ODBC, en caso de que se utilice. Para las aplicaciones que no sean secuencias de comandos, se puede crear un DSN de usuario en el Administrador de orígenes de datos ODBC. Para las secuencias de comandos que se ejecutan en IIS, debe crear un DSN de sistema; en caso contrario, las secuencias de comandos no reconocerán el origen de datos creado. Esto se aplica a cualquier aplicación de secuencias de comandos de ADO que utilice el proveedor de Microsoft OLE DB para ODBC a través de Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="3e72f-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="3e72f-120">Hacer referencia a la biblioteca de ADO</span><span class="sxs-lookup"><span data-stu-id="3e72f-120">Referencing the ADO Library</span></span>

<span data-ttu-id="3e72f-121">No está disponible con los lenguajes de secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="3e72f-121">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="3e72f-122">Controlar eventos</span><span class="sxs-lookup"><span data-stu-id="3e72f-122">Handling events</span></span>

<span data-ttu-id="3e72f-123">No está disponible con los lenguajes de secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="3e72f-123">N/A with scripting languages.</span></span>

<span data-ttu-id="3e72f-124">Los temas siguientes contienen información más específica sobre la utilización de ADO con los lenguajes de secuencias de comandos:</span><span class="sxs-lookup"><span data-stu-id="3e72f-124">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="3e72f-125">ADO en VBScript</span><span class="sxs-lookup"><span data-stu-id="3e72f-125">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="3e72f-126">ADO en JScript</span><span class="sxs-lookup"><span data-stu-id="3e72f-126">ADO in JScript</span></span>](jscript-ado-programming.md)

