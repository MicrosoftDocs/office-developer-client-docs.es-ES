---
title: Información general sobre el objeto MAPI y la interfaz
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
# <a name="mapi-object-and-interface-overview"></a>Información general sobre el objeto MAPI y la interfaz

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un objeto MAPI es una clase de objeto C++ o una estructura de datos C heredada de una o más interfaces MAPI, o colecciones de funciones relacionadas. Estas colecciones de funciones relacionadas son conocidas por los desarrolladores de C++ como funciones virtuales puras. Para una función virtual pura, MAPI proporciona solo el prototipo de función, no una implementación. Se espera que una aplicación cliente, un proveedor de servicios o MAPI proporcione esta implementación mediante la creación de una clase de objeto que hereda de la interfaz y se ajusta a las descripciones de funciones de la API de mensajería. Solo se puede crear una instancia de una interfaz MAPI a través de una clase heredada.
  
Hay muchos objetos MAPI diferentes, cada objeto que hereda de una interfaz que finalmente se hereda de la [interfaz IUnknown.](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) **IUnknown es** la interfaz base del Modelo de objetos componentes OLE (COM). Proporciona a los objetos MAPI un mecanismo estándar para la comunicación y el control. COM determina cómo los implementadores de objetos controlan problemas como la administración de memoria, la administración de parámetros y el multithreading. Al cumplir con este modelo, un implementador de objetos se adhiere a un contrato según lo especificado por las interfaces incluidas en el objeto. 
  
Muchas interfaces MAPI se heredan directamente de **IUnknown,** mientras que otras se heredan indirectamente a través de una de las otras dos interfaces base: [IMAPIProp : IUnknown](imapipropiunknown.md) para la administración de propiedades e [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para el acceso a carpetas y libretas de direcciones. Las interfaces base nunca se implementan como objetos independientes; siempre se implementan como parte de otros objetos, objetos que implementan interfaces derivadas. 
  
MAPI define muchos tipos de objetos, cada uno implementado por uno o más componentes MAPI. Mapi, los proveedores de servicios y los componentes de formulario personalizados usan los objetos implementados por los clientes. Los objetos implementados por los proveedores de servicios normalmente los usan MAPI y los clientes. Otros componentes de formularios y clientes usan objetos implementados por proveedores de bibliotecas de formularios y servidores de formularios. 
  
## <a name="see-also"></a>Consulte también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Conceptos de MAPI](mapi-concepts.md)

