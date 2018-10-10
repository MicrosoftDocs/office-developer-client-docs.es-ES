---
title: 'Capítulo 14: Conceptos básicos de ADO MD'
TOCTitle: 'Chapter 14: ADO MD Fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d595136c229234dfa0cb04a44fbe45f58cd79fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484241"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="c73a1-102">Capítulo 14: Conceptos básicos de ADO MD</span><span class="sxs-lookup"><span data-stu-id="c73a1-102">Chapter 14: ADO MD Fundamentals</span></span>


<span data-ttu-id="c73a1-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c73a1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c73a1-p101">Microsoft ActiveX Data Objects (MultiDimensional) (ADO MD) proporciona acceso sencillo a datos multidimensionales de lenguajes como Microsoft Visual Basic, Microsoft Visual C++ y Microsoft Visual J++. ADO MD es una ampliación de Microsoft ActiveX Data Objects (ADO) que incluye objetos específicos de datos multidimensionales, como los objetos [CubeDef](cubedef-object-ado-md.md) y [Cellset](cellset-object-ado-md.md). Con ADO MD, puede explorar un esquema multidimensional, consultar un cubo y recuperar los resultados.</span><span class="sxs-lookup"><span data-stu-id="c73a1-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="c73a1-p102">Al igual que ADO, ADO MD usa un proveedor OLE DB subyacente para obtener acceso a datos. Para trabajar con ADO MD, debe usarse un proveedor de datos multidimensionales (MDP) según se define en las especificaciones de OLE DB para OLAP. Los proveedores de datos multidimensionales presentan datos en vistas multidimensionales, al contrario que los proveedores de datos tabulares (TDP), que presentan datos en vistas tabulares. Vea la documentación correspondiente de su proveedor OLE DB para OLAP para obtener información más detallada acerca de la sintaxis y los comportamientos específicos que admite su proveedor.</span><span class="sxs-lookup"><span data-stu-id="c73a1-p102">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="c73a1-p103">En este documento, se supone que se tiene un conocimiento práctico del lenguaje de programación Visual Basic y conocimientos generales de ADO y de OLAP. Para obtener más información, vea la [Guía del programador de ADO](ado-programmer-s-guide.md) y la Referencia del programador de OLE DB para OLAP. Para obtener más información general acerca de ADO MD, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c73a1-p103">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP. For more information, see the [ADO Programmer's Guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference. For more overview information about ADO MD, see the following topics:</span></span>

  - [<span data-ttu-id="c73a1-114">Descripción general de esquemas y datos multidimensionales</span><span class="sxs-lookup"><span data-stu-id="c73a1-114">Overview of Multidimensional Schemas and Data</span></span>](overview-of-multidimensional-schemas-and-data.md)

  - [<span data-ttu-id="c73a1-115">Trabajar con datos multidimensionales</span><span class="sxs-lookup"><span data-stu-id="c73a1-115">Working with Multidimensional Data</span></span>](working-with-multidimensional-data.md)

  - [<span data-ttu-id="c73a1-116">Utilizar ADO con ADO MD</span><span class="sxs-lookup"><span data-stu-id="c73a1-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)

  - [<span data-ttu-id="c73a1-117">Programar con ADO MD</span><span class="sxs-lookup"><span data-stu-id="c73a1-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)

