---
title: Funciones seguras de clúster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409303"
---
# <a name="cluster-safe-functions"></a>Funciones seguras de clúster

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
En Excel 2013, Excel puede descargar llamadas de función User-Defined (UDF) a un clúster informático de alto rendimiento a través de una interfaz de conector de clúster dedicada. Los proveedores de clústeres de cálculo proporcionan conectores de clúster. Los autores de UDF pueden declarar sus UDF como seguras para clústeres y, cuando hay un conector de clúster presente, Excel envía llamadas a estas UDF al conector del clúster para su descarga.
  
Cuando Excel detecta una UDF segura para clústeres durante el recálculo, pasa el nombre del XLL que se está ejecutando actualmente, el nombre de la UDF segura para clústeres y cualquier parámetro al conector del clúster. El conector ejecuta la llamada UDF de forma remota y devuelve los resultados a Excel. El cálculo no dependiente continúa y cuando el conector de clúster ha terminado de ejecutar la UDF, pasa los resultados a Excel y los cálculos dependientes continúan. El mecanismo de este comportamiento asincrónico imita el mecanismo usado por las UDF asincrónicas, excepto que el conector de clúster administra los aspectos asincrónicos en lugar del autor de UDF. Normalmente, un conector de clúster implementa una corrección XLL para cargar XLL y ejecutar UDF en nodos de clúster de proceso.
  
La mecánica de declarar UDF como segura para clústeres es similar a la de declarar UDF como segura para el recálculo multiproceso. Sin embargo, dado que la UDF no se ejecuta necesariamente en el mismo equipo que otras UDF de la misma sesión de Excel, hay diferentes consideraciones al escribir UDF seguras para clústeres.
  
Para registrar una UDF como segura para clústeres, debe llamar a la función de devolución de llamada [xlfRegister (formulario 1)](xlfregister-form-1.md) a través de la interfaz **de Excel12** **o Excel12v.** Para obtener más información acerca de estas interfaces, vea [Excel4/Excel12](excel4-excel12.md) y [Excel4v/Excel12v](excel4v-excel12v.md). No se admite el registro de una UDF como segura para clústeres a través de la interfaz de **Excel4** o **Excel4v.** 
  
Si registra una función como segura para clústeres, debe asegurarse de que la función se comporta de forma segura para clústeres. Aunque el comportamiento exacto del conector de clúster es específico de la implementación, debe diseñar la UDF para que se ejecute en un sistema de equipo distribuido y que tenga las siguientes características:
  
- Una UDF no debe depender de ningún estado de memoria. Por ejemplo, una UDF no debe depender de una memoria caché en memoria existente.
    
- Una UDF no debe realizar devoluciones Excel que el proveedor de conectores de clúster no admite.
    
Además del comportamiento seguro para clústeres, existen las siguientes restricciones técnicas en las UDF seguras para clústeres:
  
1. No hay argumentos XLOPER (tipos 'P', 'R').
    
2. No hay argumentos XLOPER12 que admitan referencias de intervalo (tipo 'U').
    
3. No se puede combinar una función equivalente de hoja de macros ('#' y &amp; ' ').
    
Para las UDF con tiempos de ejecución más cortos, la sobrecarga de descarga puede ser mayor que el tiempo que tarda la UDF en ejecutarse, lo que niega muchas de las ventajas de usar esta infraestructura.
  
> [!NOTE]
> No puede declarar una UDF segura para clústeres como UDF asincrónica. 
  
Una UDF puede determinar si se ejecuta con un conector de clúster llamando a la función de devolución de llamada [xlRunningOnCluster.](xlrunningoncluster.md) 
  

