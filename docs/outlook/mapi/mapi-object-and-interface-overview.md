---
title: Objeto MAPI e Introducción a la interfaz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4f69985f9cdaaba0681b823e6fe448d009ee9dfa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585713"
---
# <a name="mapi-object-and-interface-overview"></a>Objeto MAPI e Introducción a la interfaz

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un objeto MAPI es una clase de objeto de C++ o C estructura de datos se hereda de una o más interfaces MAPI o colecciones de funciones relacionadas. Estas colecciones de funciones relacionadas se conocen los desarrolladores de C++ como funciones virtuales puras. Para una función virtual pura, MAPI proporciona solo el prototipo de función, no una implementación. Se espera que una aplicación cliente, un proveedor de servicios o MAPI proporcionará esta implementación mediante la creación de una clase de objeto que hereda de la interfaz y se ajusta a las descripciones de la función de la API de mensajería. Una interfaz de MAPI se puede crear instancias sólo a través de una clase heredada.
  
Hay muchos objetos MAPI diferentes, cada objeto que herede de una interfaz que se hereda en última instancia de la interfaz [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) . **IUnknown** es la interfaz base OLE componente modelo de objetos (COM). Proporciona objetos MAPI con un mecanismo estándar para la comunicación y control. COM determina cómo los implementadores del objeto resolver problemas como la administración de memoria, la administración de parámetro y el subprocesamiento múltiple. De forma que se ajusten a este modelo, un implementador de objeto se ajusta a un contrato tal como se especifica mediante las interfaces que se incluyen en el objeto. 
  
Muchas de las interfaces MAPI se heredan directamente de **IUnknown**, mientras que otras personas se heredan indirectamente a través de una de las otras dos interfaces bases: [IMAPIProp: IUnknown](imapipropiunknown.md) para la administración de propiedad y [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para la carpeta y acceso a la libreta de direcciones. Interfaces base nunca se implementan como objetos independientes, de independiente; siempre se implementan como parte de otros objetos, los objetos que implementan interfaces derivan. 
  
MAPI define muchos tipos de objetos, cada uno implementado por uno o más componentes MAPI. Se utilizan objetos implementados por los clientes MAPI, proveedores de servicios y componentes de formularios personalizados. Objetos que implementan los proveedores de servicio se usan normalmente por MAPI y por los clientes. Objetos implementan los proveedores de la biblioteca de formulario y los servidores de formulario se usan por otros componentes de formulario y por los clientes. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Conceptos MAPI](mapi-concepts.md)

