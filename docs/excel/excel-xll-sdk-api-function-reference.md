---
title: Referencia de funciones de API de SDK de XLL de Excel 2013
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referencia de la función API [excel 2007], funciones [Excel 2007], referencia [Excel 2007], Kit de desarrollo de Software de XLL de Excel 2007, referencia
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815628"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Referencia de funciones de API de SDK de XLL de Excel 2013

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
El SDK de XLL de Microsoft Excel 2013 contiene los archivos de origen para una biblioteca de Framework que está diseñado para acelerar la escritura de los XLL y dos proyectos de ejemplo, ejemplo y genérico. 
  
En esta sección se proporciona una referencia a la función para lo siguiente:
  
- Las devoluciones de llamada que se puede llamar a los XLL de Excel.
    
- Devoluciones de llamada XLL que busca Microsoft Excel.
    
- Funciones clave en los proyectos de ejemplo y framework.
    
## <a name="sample-projects"></a>Proyectos de ejemplo

El SDK de XLL de Excel 2013 proporciona archivos de origen y los archivos de proyecto de Microsoft Visual Studio para los proyectos de ejemplo siguiente:
  
- El proyecto **Framework** (`SAMPLES\FRAMEWRK\`) contiene un proyecto que puede crearse en una biblioteca, FRAMEWRK.lib, que, a continuación, se pueden vincular a otros proyectos XLL. La biblioteca contiene muchas funciones y herramientas que hacen que escribir XLL sea más fáciles. Esta biblioteca se usa en ambos de los otros proyectos junto con el archivo de encabezado FRAMEWRK.h.
    
- El proyecto de **ejemplo** (`SAMPLES\EXAMPLE\`) contiene un proyecto que puede crearse para un XLL, EXAMPLE.xll. El XLL contiene muchos ejemplos del uso de la biblioteca de Framework y las implementaciones de ejemplo de las funciones de la interfaz del complemento de XLL como **xlAutoOpen**.
    
- El proyecto **genérico** (`SAMPLES\GENERIC\`) contiene un proyecto que puede crearse para un XLL, GENERIC.xll. El XLL muestra varias funciones de ejemplo y los comandos y es un buen punto de partida para escribir su propia XLL.
    
## <a name="in-this-section"></a>En esta sección

- [Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)
  
- [Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)
  
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)
  
- [Funciones de la DLL genérica](functions-in-the-generic-dll.md)
  
- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Vea también

- [Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
  
- [Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

