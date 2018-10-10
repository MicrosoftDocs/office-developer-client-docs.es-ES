---
title: 'Capítulo 15: Conceptos básicos de ADOX'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3869f23b93df78fd207812a85f91dd3272bd255f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486389"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="4f22d-102">Capítulo 15: Conceptos básicos de ADOX</span><span class="sxs-lookup"><span data-stu-id="4f22d-102">Chapter 15: ADOX Fundamentals</span></span>


<span data-ttu-id="4f22d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f22d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4f22d-p101">Microsoft® ActiveX® Extensiones de ADO para lenguaje de definición de datos y seguridad (ADOX) es una extensión de los objetos y el modelo de programación de ADO. ADOX incluye objetos para creación y modificación de esquemas, así como de seguridad. Dado que se trata de un enfoque basado en objetos para la manipulación de esquemas, se puede escribir código que funcionará con diversos orígenes de datos, independientemente de las diferencias de sus sintaxis nativas.</span><span class="sxs-lookup"><span data-stu-id="4f22d-p101">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="4f22d-p102">ADOX es una biblioteca complementaria a los objetos ADO básicos. Expone objetos adicionales para crear, modificar y eliminar objetos de esquema, como tablas y procedimientos. También incluye objetos de seguridad para mantener usuarios y grupos, y para conceder y revocar permisos en objetos.</span><span class="sxs-lookup"><span data-stu-id="4f22d-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="4f22d-p103">Para utilizar ADOX con su herramienta de desarrollo, debe establecer una referencia a la biblioteca de tipos ADOX. La descripción de la biblioteca ADOX es "Microsoft ADO Ext. para DDL y seguridad". El nombre de archivo de biblioteca ADOX es Msadox.dll y el identificador de programa (ProgID) es "ADOX". Para obtener más información acerca del establecimiento de referencias a bibliotecas, vea la documentación de su herramienta de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="4f22d-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="4f22d-p104">El Proveedor OLE DB de Microsoft para el motor de base de datos Microsoft Jet es totalmente compatible con ADOX. Es posible que algunas características de ADOX no sean compatibles, dependiendo de cuál sea su proveedor de datos. Para obtener más información acerca de las características compatibles con el Proveedor OLE DB de Microsoft para ODBC, el Proveedor OLE DB de Microsoft para Oracle o el Proveedor OLE DB de Microsoft para SQL Server, vea el archivo Léame de MDAC.</span><span class="sxs-lookup"><span data-stu-id="4f22d-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="4f22d-p105">En este documento, se supone que se tiene un conocimiento práctico del lenguaje de programación Microsoft® Visual Basic® y conocimientos generales de ADO. Para obtener más información acerca de ADO, vea la [Guía del programador de ADO](ado-programmer-s-guide.md). Para obtener más información general acerca de ADOX, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="4f22d-p105">This document assumes a working knowledge of the Microsoft® Visual Basic® programming language and a general knowledge of ADO. For more information about ADO, see the [ADO Programmer's Guide](ado-programmer-s-guide.md). For more overview information about ADOX, see the following topics:</span></span>

  - [<span data-ttu-id="4f22d-120">Objetos de ADOX</span><span class="sxs-lookup"><span data-stu-id="4f22d-120">ADOX Objects</span></span>](adox-objects.md)

  - [<span data-ttu-id="4f22d-121">Colecciones de ADOX</span><span class="sxs-lookup"><span data-stu-id="4f22d-121">ADOX Collections</span></span>](adox-collections.md)

  - [<span data-ttu-id="4f22d-122">Propiedades de ADOX</span><span class="sxs-lookup"><span data-stu-id="4f22d-122">ADOX Properties</span></span>](adox-properties.md)

  - [<span data-ttu-id="4f22d-123">Métodos de ADOX</span><span class="sxs-lookup"><span data-stu-id="4f22d-123">ADOX Methods</span></span>](adox-methods.md)

  - [<span data-ttu-id="4f22d-124">Ejemplos de ADOX</span><span class="sxs-lookup"><span data-stu-id="4f22d-124">ADOX Examples</span></span>](adox-code-examples.md)

