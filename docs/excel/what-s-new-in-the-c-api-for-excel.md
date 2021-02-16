---
title: Novedades de la API de C para Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api de c [excel 2007], novedades
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439691"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Novedades de la API de C para Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Junto con Microsoft Excel 2013, el Kit de desarrollo de software (SDK) XLL de Microsoft Excel 2013 incluye compatibilidad con las siguientes características.
  
- **Nuevas funciones**
    
    El SDK de XLL de Microsoft Excel 2013 admite la llamada a todas las nuevas funciones de hoja de cálculo de Excel 2013. Para obtener más información acerca de cómo llamar a funciones de Excel 2013, vea Llamar a Excel desde [el DLL o XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Funciones asincrónicas definidas por el usuario**
    
    Excel 2013 admite llamadas a funciones definidas por el usuario (UDF) de forma asincrónica, lo que puede mejorar el rendimiento al permitir que se ejecuten varios cálculos al mismo tiempo. Para obtener más información acerca de las UDF asincrónicas, vea Funciones de User-Defined [asincrónicas.](asynchronous-user-defined-functions.md)
    
- **Conectores de clúster**
    
    Los conectores de clúster permiten que las UDF se ejecuten en clústeres de cálculo de alto rendimiento. Para obtener más información acerca de la creación de conectores de clúster, vea [Desarrollar conectores de clúster de Excel.](developing-excel-cluster-connectors.md)
    
    > [!NOTE]
    > Los complementos XLL que desea ejecutar en clústeres de cálculo solo deben llamar a funciones seguras para clústeres. Para obtener más información acerca de las funciones que puede usar, vea Referencia de funciones de API de SDK de [XLL](excel-xll-sdk-api-function-reference.md) de Excel y [Funciones seguras de clúster.](cluster-safe-functions.md) 
  
- **Compatibilidad de 64 bits**
    
    Ahora puede compilar y vincular XLL de 32 bits y 64 bits. Para obtener más información, vea [Crear XLL.](creating-xlls.md)
    
## <a name="see-also"></a>Consulte también



[Desarrollar archivos XLL de Excel](developing-excel-xlls.md)
  
[Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
  
[Multiproceso y conflictos de memoria en Excel](multithreading-and-memory-contention-in-excel.md)


[Introducción al SDK de XLL de Excel](getting-started-with-the-excel-xll-sdk.md)

