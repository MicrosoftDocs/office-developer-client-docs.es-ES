---
title: El papel de ADO en Microsoft Data Access
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91f591513e0a35a70d157b0a640c87efc961fe22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314038"
---
# <a name="role-of-ado-in-microsoft-data-access"></a><span data-ttu-id="dc7e5-102">Rol de ADO en Microsoft Data Access</span><span class="sxs-lookup"><span data-stu-id="dc7e5-102">Role of ADO in Microsoft Data Access</span></span>

<span data-ttu-id="dc7e5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc7e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc7e5-p101">Microsoft Data Access Components (MDAC) proporciona acceso a datos que son independientes de almacenes de datos, herramientas y lenguajes. Proporciona una interfaz de alto nivel, fácil de usar y una interfaz de bajo nivel, de alto rendimiento para prácticamente cualquier almacén de datos disponible. Puede utilizar esta flexibilidad para integrar diversos almacenes de datos y usar su selección de herramientas, aplicaciones y servicios de plataforma para crear las soluciones adecuadas para sus necesidades. Estas tecnologías proporcionan el marco de trabajo básico para obtener acceso a datos generales en sistemas operativos Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dc7e5-p101">The Microsoft Data Access Components (MDAC) provide data access that is independent of data stores, tools, and languages. It provides a high-level, easy-to-use interface, and a low-level, high-performance interface to practically any data store available. You can use this flexibility to integrate diverse data stores and use your choice of tools, applications, and platform services to create the right solutions for your needs. These technologies provide the basic framework for general-purpose data access in Microsoft Windows operating systems.</span></span>

<span data-ttu-id="dc7e5-p102">MDAC consta de tres tecnologías principales. ActiveX Data Objects (ADO) es una interfaz de nivel alto, fácil de usar, para OLE DB. OLE DB es una interfaz de bajo nivel y alto rendimiento para una variedad de almacenes de datos. Tanto ADO como OLE DB pueden trabajar con datos relacionales (tabulares) y no relacionales (jerárquicos o de secuencia). Por último, ODBC (conectividad de base de datos abierta) es otra interfaz de bajo nivel y alto rendimiento, diseñada específicamente para almacenes de datos relacionales.</span><span class="sxs-lookup"><span data-stu-id="dc7e5-p102">There are three primary technologies in MDAC. ActiveX Data Objects (ADO) is a high-level, easy-to-use interface to OLE DB. OLE DB is a low-level, high-performance interface to a variety of data stores. ADO and OLE DB both can work with relational (tabular) and nonrelational (hierarchical or stream) data. Finally, Open Database Connectivity (ODBC) is another low-level, high-performance interface that is designed specifically for relational data stores.</span></span>

<span data-ttu-id="dc7e5-p103">ADO proporciona una capa de abstracción entre la aplicación de cliente o de nivel intermedio y las interfaces OLE DB de bajo nivel. ADO utiliza un pequeño conjunto de objetos de automatización para proporcionar una interfaz sencilla y eficaz a OLE DB. Esta interfaz hace de ADO la elección perfecta para los programadores en lenguajes de mayor nivel, como Visual Basic e incluso VBScript, que desean tener acceso a datos sin tener que aprender las complejidades de COM y OLE DB.</span><span class="sxs-lookup"><span data-stu-id="dc7e5-p103">ADO provides a layer of abstraction between your client or middle-tier application and the low-level OLE DB interfaces. ADO uses a small set of Automation objects to provide a simple and efficient interface to OLE DB. This interface makes ADO the perfect choice for developers in higher level languages, such as Visual Basic and even VBScript, who want to access data without having to learn the intricacies of COM and OLE DB.</span></span>

