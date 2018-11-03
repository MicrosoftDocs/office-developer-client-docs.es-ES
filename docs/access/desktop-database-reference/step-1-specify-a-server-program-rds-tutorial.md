---
title: 'Paso 1: Especificar un programa de servidor (Tutorial de RDS)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5bd5e8edc17eb482177d97cb82611a8b6b12d0a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946058"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a><span data-ttu-id="1d6b3-102">Paso 1: Especificar un programa de servidor (Tutorial de RDS)</span><span class="sxs-lookup"><span data-stu-id="1d6b3-102">Step 1: Specify a server program (RDS Tutorial)</span></span>

<span data-ttu-id="1d6b3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d6b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d6b3-p101">En el caso más general, use el método [CreateObject](createobject-method-rds.md) del objeto [RDS.DataSpace](dataspace-object-rds.md) para especificar el programa predeterminado de servidor, [RDSServer.DataFactory](datafactory-object-rdsserver.md), o su propio programa de servidor personalizado (objeto de negocio). Se crea entonces una instancia del programa de servidor en el servidor y se devuelve una referencia (o *proxy*) al programa de servidor.</span><span class="sxs-lookup"><span data-stu-id="1d6b3-p101">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="1d6b3-106">Este tutorial utiliza el programa de servidor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="1d6b3-106">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

