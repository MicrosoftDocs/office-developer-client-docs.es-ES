---
title: 'Capítulo 14: Conceptos básicos de ADO MD'
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44a4e666fb615f7d3870acfbd986e93971606d5b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701140"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="385bc-102">Capítulo 14: Conceptos básicos de ADO MD</span><span class="sxs-lookup"><span data-stu-id="385bc-102">Chapter 14: ADO MD fundamentals</span></span>

<span data-ttu-id="385bc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="385bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="385bc-p101">Microsoft ActiveX Data Objects (MultiDimensional) (ADO MD) proporciona acceso sencillo a datos multidimensionales de lenguajes como Microsoft Visual Basic, Microsoft Visual C++ y Microsoft Visual J++. ADO MD es una ampliación de Microsoft ActiveX Data Objects (ADO) que incluye objetos específicos de datos multidimensionales, como los objetos [CubeDef](cubedef-object-ado-md.md) y [Cellset](cellset-object-ado-md.md). Con ADO MD, puede explorar un esquema multidimensional, consultar un cubo y recuperar los resultados.</span><span class="sxs-lookup"><span data-stu-id="385bc-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="385bc-p102">Al igual que ADO, ADO MD usa un proveedor OLE DB subyacente para obtener acceso a datos. Para trabajar con ADO MD, debe usarse un proveedor de datos multidimensionales (MDP) según se define en las especificaciones de OLE DB para OLAP. Los proveedores de datos multidimensionales presentan datos en vistas multidimensionales, al contrario que los proveedores de datos tabulares (TDP), que presentan datos en vistas tabulares. Vea la documentación correspondiente de su proveedor OLE DB para OLAP para obtener información más detallada acerca de la sintaxis y los comportamientos específicos que admite su proveedor.</span><span class="sxs-lookup"><span data-stu-id="385bc-p102">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="385bc-111">En este documento, se supone que se tiene un conocimiento práctico del lenguaje de programación Visual Basic y conocimientos generales de ADO y de OLAP.</span><span class="sxs-lookup"><span data-stu-id="385bc-111">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</span></span> <span data-ttu-id="385bc-112">Para obtener más información, consulte la [Guía del programador de ADO](ado-programmer-s-guide.md) y OLE DB para la referencia del programador de OLAP.</span><span class="sxs-lookup"><span data-stu-id="385bc-112">For more information, see the [ADO programmer's guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference.</span></span> 

<span data-ttu-id="385bc-113">En este capítulo, se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="385bc-113">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="385bc-114">Información general de los esquemas y datos multidimensionales</span><span class="sxs-lookup"><span data-stu-id="385bc-114">Overview of multidimensional schemas and data</span></span>](overview-of-multidimensional-schemas-and-data.md)
- [<span data-ttu-id="385bc-115">Trabajar con datos multidimensionales</span><span class="sxs-lookup"><span data-stu-id="385bc-115">Working with multidimensional data</span></span>](working-with-multidimensional-data.md)
- [<span data-ttu-id="385bc-116">Utilizar ADO con ADO MD</span><span class="sxs-lookup"><span data-stu-id="385bc-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)
- [<span data-ttu-id="385bc-117">Programar con ADO MD</span><span class="sxs-lookup"><span data-stu-id="385bc-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)
