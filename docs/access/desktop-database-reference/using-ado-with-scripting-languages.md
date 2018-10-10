---
title: Utilizar ADO con lenguajes de secuencias de comandos
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2de5cd9507ede3308a207b078a5bc66a4917e267
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486663"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="2657c-102">Utilizar ADO con lenguajes de secuencias de comandos</span><span class="sxs-lookup"><span data-stu-id="2657c-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="2657c-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2657c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2657c-p101">En un entorno de scripting, ADO permite exponer datos mediante scripting de servidor. En este escenario, ADO, el proveedor OLE DB subyacente que usa y cualquier otro componente necesario para hacer referencia a un almacén de datos determinado están instalados en un servidor que ejecuta Internet Information Services(IIS). Con páginas Active Server (ASP), ADO es un componente al que se hace referencia en un script que puede generar, por ejemplo, contenido HTML. Este contenido HTML se puede pasar a un explorador web de cliente a través de HTTP. En un entorno de scripting, ADO permite exponer datos mediante scripting de servidor. En este escenario, se instala en un servidor con Internet Information Services (IIS): ADO, el proveedor OLE DB subyacente que usa, y muchos otros componentes necesarios para hacer referencia a un determinado almacén de datos. ADO, que usa páginas Active Server (ASP), es un componente al que se hace referencia en un script que puede generar HTML, por ejemplo. Este contenido HTML se puede pasar mediante HTTP a un explorador web de cliente. Mediante el uso de scripting, la página web puede enviar acciones al script de servidor, lo que permite actualizar, atravesar o consultar datos específicos.</span><span class="sxs-lookup"><span data-stu-id="2657c-p101">Within a scripting environment, ADO allows you to expose data by way of server-side scripting. In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS). Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example. This HTML content can be passed via HTTP to a client Web browser. Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="2657c-109">Orígenes de datos ODBC</span><span class="sxs-lookup"><span data-stu-id="2657c-109">ODBC Data Sources</span></span>

<span data-ttu-id="2657c-p102">Una diferencia importante entre código de ADO que consta de secuencias de comandos y código de ADO que no consta de secuencias de comandos es el origen de datos ODBC, en caso de que se utilice. Para las aplicaciones que no sean secuencias de comandos, se puede crear un DSN de usuario en el Administrador de orígenes de datos ODBC. Para las secuencias de comandos que se ejecutan en IIS, debe crear un DSN de sistema; en caso contrario, las secuencias de comandos no reconocerán el origen de datos creado. Esto se aplica a cualquier aplicación de secuencias de comandos de ADO que utilice el proveedor de Microsoft OLE DB para ODBC a través de Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="2657c-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="2657c-114">Hacer referencia a la biblioteca de ADO</span><span class="sxs-lookup"><span data-stu-id="2657c-114">Referencing the ADO Library</span></span>

<span data-ttu-id="2657c-115">No está disponible con los lenguajes de secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="2657c-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="2657c-116">Controlar eventos</span><span class="sxs-lookup"><span data-stu-id="2657c-116">Handling events</span></span>

<span data-ttu-id="2657c-117">No está disponible con los lenguajes de secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="2657c-117">N/A with scripting languages.</span></span>

<span data-ttu-id="2657c-118">Los temas siguientes contienen información más específica sobre la utilización de ADO con los lenguajes de secuencias de comandos:</span><span class="sxs-lookup"><span data-stu-id="2657c-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="2657c-119">ADO en VBScript</span><span class="sxs-lookup"><span data-stu-id="2657c-119">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="2657c-120">ADO en JScript</span><span class="sxs-lookup"><span data-stu-id="2657c-120">ADO in JScript</span></span>](jscript-ado-programming.md)

