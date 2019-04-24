---
title: Extensiones de Visual C++ para ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302760"
---
# <a name="visual-c-extensions-for-ado"></a>Extensiones de Visual C++ para ADO


**Se aplica a:** Access 2013, Office 2013

El método preferido para programar ado con Visual c++ es usar la ** \#Directiva Import** , como se describe en [programación de ADO con Microsoft Visual c++](visual-c-ado-programming.md). Sin embargo, las versiones anteriores de ADO incluían un método alternativo de programación con Visual C++ : las Extensiones de Visual C++. Esta sección documenta esta característica para los usuarios que deben mantener el código de extensiones de Visual C++, pero el nuevo código \#ADO debe escribirse con **Import**.

Una de las tareas más tediosas a las que se enfrentan los programadores de Visual C++ a la hora de recuperar datos con ADO es convertir los datos devueltos como un tipo de datos VARIANT en un tipo de datos de C++ y después almacenar los datos convertidos en una clase o estructura. Además de ser molesto, recuperar datos de C++ a través de un tipo de datos VARIANT disminuye el rendimiento.

ADO proporciona una interfaz que admite datos recuperación de datos en tipos de datos nativos de C/C++ sin pasar por un VARIANT, y también proporciona macros de preprocesador que simplifican el uso de la interfaz. El resultado es una herramienta flexible más fácil de utilizar y con mayor rendimiento.

Un escenario común de cliente C/C++ consiste en enlazar un registro de un objeto [Recordset](recordset-object-ado.md) a una estructura o clase de C/C++ que contiene tipos nativos de C/C++. Cuando se usa el paso a través de VARIANTs, esto implica escribir código de conversión de VARIANT a tipos nativos de C/C++. Las Extensiones de Visual C++ para ADO permiten facilitar este escenario al programador de Visual C++.

Vea los temas siguientes para aprender más acerca de las Extensiones de Visual C++ para ADO.

  - [Utilizar Extensiones de Visual C++ para ADO](using-visual-c-extensions.md)

  - [Encabezado de Extensiones de Visual C++](visual-c-extensions-header.md)

  - [Ejemplo de ADO con Extensiones de Visual C++](visual-c-extensions-example.md)

