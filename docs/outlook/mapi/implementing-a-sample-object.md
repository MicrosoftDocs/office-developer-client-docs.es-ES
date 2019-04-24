---
title: Implementar un objeto de muestra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332833"
---
# <a name="implementing-a-sample-object"></a>Implementar un objeto de muestra

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los objetos de notificación de aviso (objetos que admiten la interfaz [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) ) son objetos MAPI que las aplicaciones cliente implementan para procesar notificaciones. **IMAPIAdviseSink** hereda directamente de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) y solo contiene un método, subnotify. **** Por lo tanto, para implementar un objeto de receptor de notificaciones, un cliente crea código para los tres métodos en **IUnknown** y [Notify](imapiadvisesink-onnotify.md).
  
El archivo de encabezado Mapidefs. h define una implementación de la interfaz **IMAPIAdviseSink** mediante **DECLARE_MAPI_INTERFACE**, de la siguiente manera:
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Los clientes que implementan los objetos del receptor de notificaciones pueden definir sus interfaces en sus objetos manualmente o con las macros **MAPI_IUNKNOWN_METHODS** y **MAPI_IMAPIADVISESINK_METHODS** . Los implementadores de objetos deben usar las macros de interfaz siempre que sea posible para garantizar la coherencia entre los objetos y ahorrar tiempo y esfuerzo. 
  
La implementación de los métodos [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) y [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) es relativamente sencilla porque normalmente solo se necesitan unas pocas líneas de código. Por lo tanto, los clientes y los proveedores de servicios que implementan objetos pueden realizar sus implementaciones **AddRef** y **Release** en línea. El código siguiente muestra cómo definir un objeto receptor de notificaciones de C++ con implementaciones en línea de **AddRef** y **Release**.
  
```cpp
class  CMAPIAdviseSink : public IMAPIAdviseSink
{
public:
    STDMETHODIMP QueryInterface
                    (REFIID                     riid,
                     LPVOID *                   ppvObj);
    inline STDMETHODIMP_(ULONG) AddRef
                    () { InterlockedIncrement(m_cRef);
                         ++m_cRef;
                         InterlockedDecrement(m_cRef);
                         return m_cRef; };
    inline STDMETHODIMP_(ULONG) Release
                    () { InterlockedIncrement(m_cRef);
                         ULONG ulCount = --m_cRef;
                         InterlockedDecrement(m_cRef);
                         if (!ulCount)  delete this;
                         return ulCount;};
    MAPI_IMAPIADVISESINK_METHODS(IMPL);
    BOOL WINAPI AddConnection (LPMDB pMDBObj, ULONG ulConnection);
    void WINAPI RemoveAllLinks (LPMDB pMDBObj);
// Constructors and destructors.
public :
    inline CMAPIAdviseSink  (CStoreClient * pStore)
                            { m_cRef = 1;
                              m_ulConnection = 0;
                              m_pStore = pStore;
                              AddRef;};
    ~CMAPIAdviseSink () {Release};
private :
    ULONG               m_cRef;
    CStoreClient *      m_pStore;
    ULONG               m_ulConnection;
};
 
```

En C, el objeto de notificación de aviso está compuesto por los siguientes elementos:
  
- Un puntero a una vtable que contiene punteros a las implementaciones de cada uno de los métodos en **IUnknown** y **IMAPIAdviseSink**.
    
- Miembros de datos.
    
En el ejemplo de código siguiente se muestra cómo definir un objeto de receptor de notificaciones en C y construir su vtable. 
  
```cpp
// Object definition.
typedef struct _ADVISESINK
{
    const ADVISE_Vtbl FAR *    lpVtbl;
    ULONG             cRef;
    STORECLIENT      *pStore;
    ULONG             ulConnection;
} ADVISESINK, *LPADVISESINK;
// vtable definition.
static const ADVISE_Vtbl vtblADVISE =
{
    ADVISE_QueryInterface,
    ADVISE_AddRef,
    ADVISE_Release,
    ADVISE_OnNotify
};
 
```

Después de declarar un objeto en C, debe inicializarlo estableciendo el puntero vtable en la dirección de la vtable construida, como se muestra en el código siguiente:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)
- [Implementación de objetos MAPI](implementing-mapi-objects.md)

