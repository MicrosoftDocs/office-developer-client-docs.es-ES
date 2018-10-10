---
title: Extensiones de Visual C++ para ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7d3a5e876dd98e26c2eb9169a21a8dcd5e532e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485581"
---
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="87a18-102">Extensiones de Visual C++ para ADO</span><span class="sxs-lookup"><span data-stu-id="87a18-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="87a18-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="87a18-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="87a18-104">El método preferido de programación ADO con Visual C++ es utilizar el \*\* \#importar\*\* directiva, como se describe en [Programación ADO en Microsoft Visual C++](visual-c-ado-programming.md).</span><span class="sxs-lookup"><span data-stu-id="87a18-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="87a18-105">Sin embargo, las versiones anteriores de ADO incluían un método alternativo de programación con Visual C++ : las Extensiones de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="87a18-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="87a18-106">Esta sección documenta esa característica para aquéllos que deben mantener código de extensiones de Visual C++, pero se debe escribir el nuevo código de ADO con \# **Importar**.</span><span class="sxs-lookup"><span data-stu-id="87a18-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="87a18-p102">Una de las tareas más tediosas a las que se enfrentan los programadores de Visual C++ a la hora de recuperar datos con ADO es convertir los datos devueltos como un tipo de datos VARIANT en un tipo de datos de C++ y después almacenar los datos convertidos en una clase o estructura. Además de ser molesto, recuperar datos de C++ a través de un tipo de datos VARIANT disminuye el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="87a18-p102">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure. In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="87a18-p103">ADO proporciona una interfaz que admite datos recuperación de datos en tipos de datos nativos de C/C++ sin pasar por un VARIANT, y también proporciona macros de preprocesador que simplifican el uso de la interfaz. El resultado es una herramienta flexible más fácil de utilizar y con mayor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="87a18-p103">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface. The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="87a18-p104">Un escenario común de cliente C/C++ consiste en enlazar un registro de un objeto [Recordset](recordset-object-ado.md) a una estructura o clase de C/C++ que contiene tipos nativos de C/C++. Cuando se usa el paso a través de VARIANTs, esto implica escribir código de conversión de VARIANT a tipos nativos de C/C++. Las Extensiones de Visual C++ para ADO permiten facilitar este escenario al programador de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="87a18-p104">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types. When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types. The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="87a18-114">Vea los temas siguientes para aprender más acerca de las Extensiones de Visual C++ para ADO.</span><span class="sxs-lookup"><span data-stu-id="87a18-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="87a18-115">Utilizar Extensiones de Visual C++ para ADO</span><span class="sxs-lookup"><span data-stu-id="87a18-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="87a18-116">Encabezado de Extensiones de Visual C++</span><span class="sxs-lookup"><span data-stu-id="87a18-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="87a18-117">Ejemplo de ADO con Extensiones de Visual C++</span><span class="sxs-lookup"><span data-stu-id="87a18-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)
