---
title: Implementación de un objeto de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396795"
---
# <a name="implementing-a-sample-object"></a>Implementación de un objeto de ejemplo

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Objetos del receptor de aviso: los objetos que admiten la [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interfaz — son MAPI objetos que implementan las aplicaciones cliente para procesar las notificaciones. **IMAPIAdviseSink** hereda directamente de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) y contiene un solo método, **OnNotify**. Por lo tanto, para implementar un objeto de receptor advise, un cliente crea código para los tres métodos de **IUnknown** y para [OnNotify](imapiadvisesink-onnotify.md).
  
El archivo de encabezado Mapidefs.h define una implementación de interfaz **IMAPIAdviseSink** utilizando **DECLARE_MAPI_INTERFACE**, como se indica a continuación:
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Los clientes que implementan de aviso receptor objetos pueden definir sus interfaces en sus objetos manualmente o con las macros **MAPI_IUNKNOWN_METHODS** y **MAPI_IMAPIADVISESINK_METHODS** . Los implementadores de objeto deben utilizar las macros de interfaz siempre que sea posible para garantizar la coherencia entre objetos y para ahorrar tiempo y esfuerzo. 
  
Implementación de los métodos de [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) es relativamente simple, debido a que normalmente se necesitan sólo unas pocas líneas de código. Por lo tanto, los clientes y proveedores de servicios que implementan objetos pueden hacer que sus implementaciones de **AddRef** y **Release** en línea. El código siguiente muestra cómo definir un C++ objeto receptor con implementaciones en línea de **AddRef** y **Release**de aviso.
  
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

En C, el objeto de receptor de advise se compone de los siguientes elementos:
  
- Un puntero a una tabla virtual que contiene punteros a las implementaciones de cada uno de los métodos de **IUnknown** y **IMAPIAdviseSink**.
    
- Miembros de datos.
    
En el ejemplo de código siguiente se muestra cómo definir un objeto de receptor advise en C y construir su tabla vtable. 
  
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

Después de declarar un objeto de C, debe inicializar estableciendo el puntero vtable en la dirección de la tabla vtable construida, tal como se muestra en el siguiente código:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)
- [Implementar objetos MAPI](implementing-mapi-objects.md)

