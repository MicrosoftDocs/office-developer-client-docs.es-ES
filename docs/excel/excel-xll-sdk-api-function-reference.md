---
title: Referencia de funciones de API de SDK de XLL de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referencia de la función API [excel 2007], funciones [Excel 2007], referencia [Excel 2007], kit de desarrollo de Software de XLL Excel 2007, referencia
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304126"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Referencia de funciones de API de SDK de XLL de Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
SDK de XLL de Microsoft Excel 2013 contiene archivos de origen de una biblioteca de marcos diseñados para acelerar la escritura de XLL, además de dos proyectos de ejemplo, Ejemplo y Genérico. 
  
Esta sección proporciona una referencia de función para lo siguiente:
  
- Devolución de llamadas de Excel a las que puede llamar XLL.
    
- Devolución de llamadas de XLL que busca Microsoft Excel.
    
- Funciones claves de los proyectos de ejemplo y de marco.
    
## <a name="sample-projects"></a>Proyectos de ejemplo

El SDK de XLL de Excel 2013 proporciona archivos de origen y archivos de proyecto de Microsoft Visual Studio para los proyectos de ejemplo siguientes:
  
- El proyecto **Framework** (`SAMPLES\FRAMEWRK\`) contiene un proyecto que puede crearse en una biblioteca, FRAMEWRK.lib, y que, después, puede vincularse a otros proyectos XLL. La biblioteca contiene muchas funciones y herramientas que facilitan la escritura de XLL. Esta biblioteca se usa en los otros dos proyectos junto con el archivo de encabezado FRAMEWRK.h.
    
- El proyecto **Example** (`SAMPLES\EXAMPLE\`) contiene un proyecto que puede crearse en un XLL, EXAMPLE.xll. El XLL contiene varios ejemplos del uso de la biblioteca de marcos y las implementaciones de ejemplo de las funciones de la interfaz del complemento XLL, como **xlAutoOpen**.
    
- El proyecto **Generic** (`SAMPLES\GENERIC\`) contiene un proyecto que puede crearse en un XLL, GENERIC.xll. El XLL muestra varias funciones y comandos de ejemplo y es un buen punto de partida para escribir sus propios XLL.
    
## <a name="in-this-section"></a>En esta sección

- [Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)
  
- [Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)
  
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)
  
- [Funciones en la DLL genérica](functions-in-the-generic-dll.md)
  
- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Vea también

- [Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
  
- [Desarrollo de XLL de Excel](developing-excel-xlls.md)

