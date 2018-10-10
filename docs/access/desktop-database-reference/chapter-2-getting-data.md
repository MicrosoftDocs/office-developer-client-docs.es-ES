---
title: 'Capítulo 2: Obtener datos'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d3df907e1dbe220caab58541b7c3eba605ef2f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485307"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="756a9-102">Capítulo 2: Obtener datos</span><span class="sxs-lookup"><span data-stu-id="756a9-102">Chapter 2: Getting Data</span></span>


<span data-ttu-id="756a9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="756a9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="756a9-p101">En el capítulo anterior, se presentaron cuatro operaciones principales que tenían que ver con la creación de una aplicación de ADO: obtener datos, examinar datos, editar datos y actualizar datos. Este capítulo se centrará en los detalles de los conceptos relativos a la primera operación: obtener datos.</span><span class="sxs-lookup"><span data-stu-id="756a9-p101">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data. This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="756a9-p102">Hay varios objetos de ADO que pueden desempeñar un rol en esta operación. Primero, hay que conectarse al origen de datos usando un objeto **Connection** de ADO (que, en ocasiones, se creará implícitamente). Después, se pasan instrucciones al origen de datos acerca de lo que se desea hacer usando un objeto **Command** de ADO (que también se puede crear de forma implícita). El resultado de pasar un comando a un origen de datos y recibir su respuesta normalmente se representará con un objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="756a9-p102">Several ADO objects can play a role in this operation. First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly). Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly). The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="756a9-110">Para obtener datos, la aplicación debe estar en comunicación con un origen de datos, como DBMS, un almacén de archivos o un archivo de texto delimitado por comas.</span><span class="sxs-lookup"><span data-stu-id="756a9-110">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file.</span></span> <span data-ttu-id="756a9-111">Esta comunicación representa una *conexión* , el entorno necesario para intercambiar datos.</span><span class="sxs-lookup"><span data-stu-id="756a9-111">This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="756a9-p104">El modelo de objetos de ADO representa el concepto de una conexión con el objeto **Connection** (la base sobre la que se construye una parte importante de la funcionalidad de ADO). El propósito de un objeto **Connection** es:</span><span class="sxs-lookup"><span data-stu-id="756a9-p104">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built. The purpose of a **Connection** object is to:</span></span>

  - <span data-ttu-id="756a9-114">Definir la información que ADO necesita para comunicarse con orígenes de datos y crear sesiones.</span><span class="sxs-lookup"><span data-stu-id="756a9-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

  - <span data-ttu-id="756a9-115">Definir las características transaccionales de la sesión.</span><span class="sxs-lookup"><span data-stu-id="756a9-115">Define the transactional capabilities of the session.</span></span>

  - <span data-ttu-id="756a9-116">Permitirle crear y ejecutar comandos en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="756a9-116">Allow you to create and execute commands against the data source.</span></span>

  - <span data-ttu-id="756a9-p105">Proporcionar información acerca del diseño del origen de datos subyacente en forma de conjuntos de filas de esquema. Para obtener más información acerca de conjuntos de filas de esquema, vea [Método OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="756a9-p105">Provide information about the design of the underlying data source in the form of schema rowsets. For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

