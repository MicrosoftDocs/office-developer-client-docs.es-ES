---
title: Desarrollo de XLL de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- complementos - [excel 2007], desarrollo de XLL - [Excel 2007], XLL - [Excel 2007], desarrollo
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701098"
---
# <a name="developing-excel-xlls"></a>Desarrollo de XLL de Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
El motivo principal para escribir XLL de Microsoft Excel y usar la API de C es crear funciones de hoja de cálculo de alto rendimiento. Las aplicaciones de funciones de alto rendimiento y, comenzando en Excel 2007, la capacidad para escribir interfaces multiproceso en recursos de servidor potentes, hacen que sea una parte muy importante de la extensibilidad de Excel. El rendimiento de XLL se mejoró aún más en Excel 2007 mediante la incorporación de nuevos tipos de datos y, lo que es más importante, la compatibilidad con multiproceso.
  
La API de C no tiene ninguna de las características de desarrollo rápido de nivel superior de Microsoft Visual Basic para Aplicaciones (VBA), COM o Microsoft .NET Framework. La administración de memoria es de bajo nivel y, por lo tanto, da mayor responsabilidad al desarrollador. Muchas características de Excel expuestas a través de COM, para que estén disponibles a través de VBA y .NET Framework, no están expuestas en la API de C.


- [Conceptos de programación de Excel](excel-programming-concepts.md)
  
- [Trabajar con DLL](working-with-dlls.md)
  
- [Obtener acceso a código XLL en Excel](accessing-xll-code-in-excel.md)
  
- [Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [Llamar a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md)
  
- [Crear XLL](creating-xlls.md)
  
- [Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Multiproceso y administración de la memoria](multithreading-and-memory-management.md)
  
- [Funciones asincrónicas definidas por el usuario](asynchronous-user-defined-functions.md)
  
- [Funciones seguras para clústeres](cluster-safe-functions.md)
  
- [Permitir interrupciones de usuarios en operaciones largas](permitting-user-breaks-in-lengthy-operations.md)
  
- [Mostrar cuadros de diálogo desde una DLL o XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Obtener acceso a la instancia de Excel y los controladores de la ventana principal](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Compatibilidad con versiones anteriores](backward-compatibility.md)
  

