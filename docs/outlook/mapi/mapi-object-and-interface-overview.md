---
title: Introducción a la interfaz y el objeto MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345790"
---
# <a name="mapi-object-and-interface-overview"></a>Introducción a la interfaz y el objeto MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un objeto MAPI es una clase de objeto de C++ o una estructura de datos de C heredada de una o varias interfaces MAPI o colecciones de funciones relacionadas. Estas colecciones de funciones relacionadas son conocidas para los programadores de C++ como funciones virtuales puras. Para una función virtual pura, MAPI proporciona solo el prototipo de función, no una implementación. Se espera que una aplicación cliente, un proveedor de servicios o MAPI proporcionen esta implementación mediante la creación de una clase de objeto que herede de la interfaz y que se ajuste a las descripciones de las funciones de la API de mensajería. Una interfaz MAPI sólo se puede instanciar a través de una clase heredada.
  
Hay muchos objetos MAPI diferentes, cada uno de los objetos que hereda de una interfaz que se hereda en última instancia desde la interfaz [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) . **IUnknown** es la interfaz base del modelo de objetos componentes (com) OLE. Proporciona objetos MAPI con un mecanismo estándar para la comunicación y el control. COM indica cómo los implementadores de objetos controlan problemas como la administración de memoria, la administración de parámetros y el subprocesamiento múltiple. Mediante la conformidad con este modelo, un implementador de objetos se adhiere a un contrato según se especifica en las interfaces incluidas en el objeto. 
  
Muchas interfaces MAPI se heredan directamente de **IUnknown**, mientras que otras se heredan indirectamente a través de una de las otras dos interfaces base: [IMAPIProp: IUnknown](imapipropiunknown.md) para la administración de propiedades y [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para Folder y acceso a la libreta de direcciones. Las interfaces base no se implementan nunca como objetos independientes independientes; siempre se implementan como parte de otros objetos, objetos que implementan interfaces derivadas. 
  
MAPI define muchos tipos de objetos, cada uno de ellos implementado por uno o varios componentes de MAPI. MAPI, los proveedores de servicios y los componentes de formulario personalizados usan los objetos que implementan los clientes. MAPI y los clientes suelen usar los objetos implementados por los proveedores de servicios. Los componentes de formularios y los clientes usan los objetos implementados por los proveedores de bibliotecas de formularios y los servidores de formularios. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Conceptos de MAPI](mapi-concepts.md)

