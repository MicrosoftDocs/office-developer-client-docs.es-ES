---
title: Novedades de la API C para Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api de c [excel 2007], novedades
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19815702"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Novedades de la API C para Excel

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Junto con Microsoft Excel 2013, el Kit de desarrollo de Software (SDK) de Microsoft Excel 2013 XLL incluye compatibilidad con las siguientes características.
  
- **Nuevas funciones**
    
    El SDK de XLL de Microsoft Excel 2013 admite la devolución de llamada para todas las nuevas funciones de hoja de cálculo en Excel 2013. Para obtener más información sobre cómo llamar a funciones de Excel 2013, consulte [Calling a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Funciones asincrónicas definidas por el usuario**
    
    Excel 2013 admite llamar a funciones definidas por el usuario (UDF) de forma asincrónica, que puede mejorar el rendimiento mediante la habilitación de varios cálculos ejecutar al mismo tiempo. Para obtener más información acerca de las UDF asincrónicas, vea [Funciones de Asynchronous User-Defined](asynchronous-user-defined-functions.md).
    
- **Conectores de clúster**
    
    Conectores de clúster de habilitar las UDF se ejecuten en clústeres de cálculo de alto rendimiento. Para obtener más información sobre la creación de conectores de clúster, vea [Desarrollo de conectores de clúster de Excel](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Los complementos XLL que va a ejecutar en clústeres de cálculo deben llamar a funciones de seguridad de clúster sólo. Para obtener más información acerca de las funciones pueden usar, vea la [Referencia de funciones de API de SDK de XLL de Excel](excel-xll-sdk-api-function-reference.md) y [Funciones seguras de clúster](cluster-safe-functions.md). 
  
- **compatibilidad con 64 bits**
    
    Ahora puede compilar y vincular los XLL de 32 bits y 64 bits. Para obtener más información, vea [Creación de XLL](creating-xlls.md).
    
## <a name="see-also"></a>Vea también



[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)
  
[Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
  
[Subprocesamiento m�ltiple y la contenci�n de memoria en Excel](multithreading-and-memory-contention-in-excel.md)


[Introducci�n al SDK de XLL de Excel 2013](getting-started-with-the-excel-xll-sdk.md)

