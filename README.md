"undefined" != typeof window && function(t, e) {
    "object" == typeof exports && "object" == typeof module ? module.exports = e() : "function" == typeof define && define.amd ? define([], e) : "object" == typeof exports ? exports.Hls = e() : t.Hls = e()
}(this, function() {
    return function(t) {
        function e(i) {
            if (r[i])
                return r[i].exports;
            var a = r[i] = {
                i: i,
                l: !1,
                exports: {}
            };
            return t[i].call(a.exports, a, a.exports, e),
            a.l = !0,
            a.exports
        }
        var r = {};
        return e.m = t,
        e.c = r,
        e.d = function(t, r, i) {
            e.o(t, r) || Object.defineProperty(t, r, {
                configurable: !1,
                enumerable: !0,
                get: i
            })
        }
        ,
        e.n = function(t) {
            var r = t && t.__esModule ? function() {
                return t.default
            }
            : function() {
                return t
            }
            ;
            return e.d(r, "a", r),
            r
        }
        ,
        e.o = function(t, e) {
            return Object.prototype.hasOwnProperty.call(t, e)
        }
        ,
        e.p = "/dist/",
        e(e.s = 29)
    }([function(t, e, r) {
        "use strict";
        function i() {}
        function a(t, e) {
            return e = "[" + t + "] > " + e
        }
        function n(t) {
            var e = c.console[t];
            return e ? function() {
                for (var r = arguments.length, i = Array(r), n = 0; n < r; n++)
                    i[n] = arguments[n];
                i[0] && (i[0] = a(t, i[0])),
                e.apply(c.console, i)
            }
            : i
        }
        function o(t) {
            for (var e = arguments.length, r = Array(e > 1 ? e - 1 : 0), i = 1; i < e; i++)
                r[i - 1] = arguments[i];
            r.forEach(function(e) {
                d[e] = t[e] ? t[e].bind(t) : n(e)
            })
        }
        r.d(e, "a", function() {
            return h
        }),
        r.d(e, "b", function() {
            return f
        });
        var s = r(5)
          , l = "function" == typeof Symbol && "symbol" == typeof Symbol.iterator ? function(t) {
            return typeof t
        }
        : function(t) {
            return t && "function" == typeof Symbol && t.constructor === Symbol && t !== Symbol.prototype ? "symbol" : typeof t
        }
          , u = {
            trace: i,
            debug: i,
            log: i,
            warn: i,
            info: i,
            error: i
        }
          , d = u
          , c = Object(s.a)()
          , h = function(t) {
            if (!0 === t || "object" === (void 0 === t ? "undefined" : l(t))) {
                o(t, "debug", "log", "info", "warn", "error");
                try {
                    d.log()
                } catch (t) {
                    d = u
                }
            } else
                d = u
        }
          , f = d
    }
    , function(t, e, r) {
        "use strict";
        var i = {
            MEDIA_ATTACHING: "hlsMediaAttaching",
            MEDIA_ATTACHED: "hlsMediaAttached",
            MEDIA_DETACHING: "hlsMediaDetaching",
            MEDIA_DETACHED: "hlsMediaDetached",
            BUFFER_RESET: "hlsBufferReset",
            BUFFER_CODECS: "hlsBufferCodecs",
            BUFFER_CREATED: "hlsBufferCreated",
            BUFFER_APPENDING: "hlsBufferAppending",
            BUFFER_APPENDED: "hlsBufferAppended",
            BUFFER_EOS: "hlsBufferEos",
            BUFFER_FLUSHING: "hlsBufferFlushing",
            BUFFER_FLUSHED: "hlsBufferFlushed",
            MANIFEST_LOADING: "hlsManifestLoading",
            MANIFEST_LOADED: "hlsManifestLoaded",
            MANIFEST_PARSED: "hlsManifestParsed",
            LEVEL_SWITCHING: "hlsLevelSwitching",
            LEVEL_SWITCHED: "hlsLevelSwitched",
            LEVEL_LOADING: "hlsLevelLoading",
            LEVEL_LOADED: "hlsLevelLoaded",
            LEVEL_UPDATED: "hlsLevelUpdated",
            LEVEL_PTS_UPDATED: "hlsLevelPtsUpdated",
            AUDIO_TRACKS_UPDATED: "hlsAudioTracksUpdated",
            AUDIO_TRACK_SWITCHING: "hlsAudioTrackSwitching",
            AUDIO_TRACK_SWITCHED: "hlsAudioTrackSwitched",
            AUDIO_TRACK_LOADING: "hlsAudioTrackLoading",
            AUDIO_TRACK_LOADED: "hlsAudioTrackLoaded",
            SUBTITLE_TRACKS_UPDATED: "hlsSubtitleTracksUpdated",
            SUBTITLE_TRACK_SWITCH: "hlsSubtitleTrackSwitch",
            SUBTITLE_TRACK_LOADING: "hlsSubtitleTrackLoading",
            SUBTITLE_TRACK_LOADED: "hlsSubtitleTrackLoaded",
            SUBTITLE_FRAG_PROCESSED: "hlsSubtitleFragProcessed",
            INIT_PTS_FOUND: "hlsInitPtsFound",
            FRAG_LOADING: "hlsFragLoading",
            FRAG_LOAD_PROGRESS: "hlsFragLoadProgress",
            FRAG_LOAD_EMERGENCY_ABORTED: "hlsFragLoadEmergencyAborted",
            FRAG_LOADED: "hlsFragLoaded",
            FRAG_DECRYPTED: "hlsFragDecrypted",
            FRAG_PARSING_INIT_SEGMENT: "hlsFragParsingInitSegment",
            FRAG_PARSING_USERDATA: "hlsFragParsingUserdata",
            FRAG_PARSING_METADATA: "hlsFragParsingMetadata",
            FRAG_PARSING_DATA: "hlsFragParsingData",
            FRAG_PARSED: "hlsFragParsed",
            FRAG_BUFFERED: "hlsFragBuffered",
            FRAG_CHANGED: "hlsFragChanged",
            FPS_DROP: "hlsFpsDrop",
            FPS_DROP_LEVEL_CAPPING: "hlsFpsDropLevelCapping",
            ERROR: "hlsError",
            DESTROYING: "hlsDestroying",
            KEY_LOADING: "hlsKeyLoading",
            KEY_LOADED: "hlsKeyLoaded",
            STREAM_STATE_TRANSITION: "hlsStreamStateTransition"
        };
        e.a = i
    }
    , function(t, e, r) {
        "use strict";
        r.d(e, "b", function() {
            return i
        }),
        r.d(e, "a", function() {
            return a
        });
        var i = {
            NETWORK_ERROR: "networkError",
            MEDIA_ERROR: "mediaError",
            KEY_SYSTEM_ERROR: "keySystemError",
            MUX_ERROR: "muxError",
            OTHER_ERROR: "otherError"
        }
          , a = {
            KEY_SYSTEM_NO_KEYS: "keySystemNoKeys",
            KEY_SYSTEM_NO_ACCESS: "keySystemNoAccess",
            KEY_SYSTEM_NO_SESSION: "keySystemNoSession",
            KEY_SYSTEM_LICENSE_REQUEST_FAILED: "keySystemLicenseRequestFailed",
            MANIFEST_LOAD_ERROR: "manifestLoadError",
            MANIFEST_LOAD_TIMEOUT: "manifestLoadTimeOut",
            MANIFEST_PARSING_ERROR: "manifestParsingError",
            MANIFEST_INCOMPATIBLE_CODECS_ERROR: "manifestIncompatibleCodecsError",
            LEVEL_LOAD_ERROR: "levelLoadError",
            LEVEL_LOAD_TIMEOUT: "levelLoadTimeOut",
            LEVEL_SWITCH_ERROR: "levelSwitchError",
            AUDIO_TRACK_LOAD_ERROR: "audioTrackLoadError",
            AUDIO_TRACK_LOAD_TIMEOUT: "audioTrackLoadTimeOut",
            FRAG_LOAD_ERROR: "fragLoadError",
            FRAG_LOAD_TIMEOUT: "fragLoadTimeOut",
            FRAG_DECRYPT_ERROR: "fragDecryptError",
            FRAG_PARSING_ERROR: "fragParsingError",
            REMUX_ALLOC_ERROR: "remuxAllocError",
            KEY_LOAD_ERROR: "keyLoadError",
            KEY_LOAD_TIMEOUT: "keyLoadTimeOut",
            BUFFER_ADD_CODEC_ERROR: "bufferAddCodecError",
            BUFFER_APPEND_ERROR: "bufferAppendError",
            BUFFER_APPENDING_ERROR: "bufferAppendingError",
            BUFFER_STALLED_ERROR: "bufferStalledError",
            BUFFER_FULL_ERROR: "bufferFullError",
            BUFFER_SEEK_OVER_HOLE: "bufferSeekOverHole",
            BUFFER_NUDGE_ON_STALL: "bufferNudgeOnStall",
            INTERNAL_EXCEPTION: "internalException"
        }
    }
    , function(t, e, r) {
        "use strict";
        r.d(e, "a", function() {
            return i
        });
        var i = Number.isFinite || function(t) {
            return "number" == typeof t && isFinite(t)
        }
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(0)
          , n = r(2)
          , o = r(1)
          , s = "function" == typeof Symbol && "symbol" == typeof Symbol.iterator ? function(t) {
            return typeof t
        }
        : function(t) {
            return t && "function" == typeof Symbol && t.constructor === Symbol && t !== Symbol.prototype ? "symbol" : typeof t
        }
          , l = new Set(["hlsEventGeneric", "hlsHandlerDestroying", "hlsHandlerDestroyed"])
          , u = function() {
            function t(e) {
                i(this, t),
                this.hls = e,
                this.onEvent = this.onEvent.bind(this);
                for (var r = arguments.length, a = Array(r > 1 ? r - 1 : 0), n = 1; n < r; n++)
                    a[n - 1] = arguments[n];
                this.handledEvents = a,
                this.useGenericHandler = !0,
                this.registerListeners()
            }
            return t.prototype.destroy = function() {
                this.onHandlerDestroying(),
                this.unregisterListeners(),
                this.onHandlerDestroyed()
            }
            ,
            t.prototype.onHandlerDestroying = function() {}
            ,
            t.prototype.onHandlerDestroyed = function() {}
            ,
            t.prototype.isEventHandler = function() {
                return "object" === s(this.handledEvents) && this.handledEvents.length && "function" == typeof this.onEvent
            }
            ,
            t.prototype.registerListeners = function() {
                this.isEventHandler() && this.handledEvents.forEach(function(t) {
                    if (l.has(t))
                        throw new Error("Forbidden event-name: " + t);
                    this.hls.on(t, this.onEvent)
                }, this)
            }
            ,
            t.prototype.unregisterListeners = function() {
                this.isEventHandler() && this.handledEvents.forEach(function(t) {
                    this.hls.off(t, this.onEvent)
                }, this)
            }
            ,
            t.prototype.onEvent = function(t, e) {
                this.onEventGeneric(t, e)
            }
            ,
            t.prototype.onEventGeneric = function(t, e) {
                var r = function(t, e) {
                    var r = "on" + t.replace("hls", "");
                    if ("function" != typeof this[r])
                        throw new Error("Event " + t + " has no generic handler in this " + this.constructor.name + " class (tried " + r + ")");
                    return this[r].bind(this, e)
                };
                try {
                    r.call(this, t, e).call()
                } catch (e) {
                    a.b.error("An internal error happened while handling event " + t + '. Error message: "' + e.message + '". Here is a stacktrace:', e),
                    this.hls.trigger(o.a.ERROR, {
                        type: n.b.OTHER_ERROR,
                        details: n.a.INTERNAL_EXCEPTION,
                        fatal: !1,
                        event: t,
                        err: e
                    })
                }
            }
            ,
            t
        }();
        e.a = u
    }
    , function(t, e, r) {
        "use strict";
        function i() {
            return "undefined" == typeof window ? self : window
        }
        e.a = i
    }
    , function(t, e, r) {
        !function(e) {
            var r = /^((?:[a-zA-Z0-9+\-.]+:)?)(\/\/[^\/\;?#]*)?(.*?)??(;.*?)?(\?.*?)?(#.*?)?$/
              , i = /^([^\/;?#]*)(.*)$/
              , a = /(?:\/|^)\.(?=\/)/g
              , n = /(?:\/|^)\.\.\/(?!\.\.\/).*?(?=\/)/g
              , o = {
                buildAbsoluteURL: function(t, e, r) {
                    if (r = r || {},
                    t = t.trim(),
                    !(e = e.trim())) {
                        if (!r.alwaysNormalize)
                            return t;
                        var a = this.parseURL(t);
                        if (!s)
                            throw new Error("Error trying to parse base URL.");
                        return a.path = o.normalizePath(a.path),
                        o.buildURLFromParts(a)
                    }
                    var n = this.parseURL(e);
                    if (!n)
                        throw new Error("Error trying to parse relative URL.");
                    if (n.scheme)
                        return r.alwaysNormalize ? (n.path = o.normalizePath(n.path),
                        o.buildURLFromParts(n)) : e;
                    var s = this.parseURL(t);
                    if (!s)
                        throw new Error("Error trying to parse base URL.");
                    if (!s.netLoc && s.path && "/" !== s.path[0]) {
                        var l = i.exec(s.path);
                        s.netLoc = l[1],
                        s.path = l[2]
                    }
                    s.netLoc && !s.path && (s.path = "/");
                    var u = {
                        scheme: s.scheme,
                        netLoc: n.netLoc,
                        path: null,
                        params: n.params,
                        query: n.query,
                        fragment: n.fragment
                    };
                    if (!n.netLoc && (u.netLoc = s.netLoc,
                    "/" !== n.path[0]))
                        if (n.path) {
                            var d = s.path
                              , c = d.substring(0, d.lastIndexOf("/") + 1) + n.path;
                            u.path = o.normalizePath(c)
                        } else
                            u.path = s.path,
                            n.params || (u.params = s.params,
                            n.query || (u.query = s.query));
                    return null === u.path && (u.path = r.alwaysNormalize ? o.normalizePath(n.path) : n.path),
                    o.buildURLFromParts(u)
                },
                parseURL: function(t) {
                    var e = r.exec(t);
                    return e ? {
                        scheme: e[1] || "",
                        netLoc: e[2] || "",
                        path: e[3] || "",
                        params: e[4] || "",
                        query: e[5] || "",
                        fragment: e[6] || ""
                    } : null
                },
                normalizePath: function(t) {
                    for (t = t.split("").reverse().join("").replace(a, ""); t.length !== (t = t.replace(n, "")).length; )
                        ;
                    return t.split("").reverse().join("")
                },
                buildURLFromParts: function(t) {
                    return t.scheme + t.netLoc + t.path + t.params + t.query + t.fragment
                }
            };
            t.exports = o
        }()
    }
    , function(t, e, r) {
        "use strict";
        var i = {
            search: function(t, e) {
                for (var r = 0, i = t.length - 1, a = null, n = null; r <= i; ) {
                    a = (r + i) / 2 | 0,
                    n = t[a];
                    var o = e(n);
                    if (o > 0)
                        r = a + 1;
                    else {
                        if (!(o < 0))
                            return n;
                        i = a - 1
                    }
                }
                return null
            }
        };
        e.a = i
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        r.d(e, "a", function() {
            return a
        });
        var a = function() {
            function t() {
                i(this, t)
            }
            return t.isBuffered = function(t, e) {
                try {
                    if (t)
                        for (var r = t.buffered, i = 0; i < r.length; i++)
                            if (e >= r.start(i) && e <= r.end(i))
                                return !0
                } catch (t) {}
                return !1
            }
            ,
            t.bufferInfo = function(t, e, r) {
                try {
                    if (t) {
                        var i = t.buffered
                          , a = []
                          , n = void 0;
                        for (n = 0; n < i.length; n++)
                            a.push({
                                start: i.start(n),
                                end: i.end(n)
                            });
                        return this.bufferedInfo(a, e, r)
                    }
                } catch (t) {}
                return {
                    len: 0,
                    start: e,
                    end: e,
                    nextStart: void 0
                }
            }
            ,
            t.bufferedInfo = function(t, e, r) {
                var i = []
                  , a = void 0
                  , n = void 0
                  , o = void 0
                  , s = void 0
                  , l = void 0;
                for (t.sort(function(t, e) {
                    var r = t.start - e.start;
                    return r || e.end - t.end
                }),
                l = 0; l < t.length; l++) {
                    var u = i.length;
                    if (u) {
                        var d = i[u - 1].end;
                        t[l].start - d < r ? t[l].end > d && (i[u - 1].end = t[l].end) : i.push(t[l])
                    } else
                        i.push(t[l])
                }
                for (l = 0,
                a = 0,
                n = o = e; l < i.length; l++) {
                    var c = i[l].start
                      , h = i[l].end;
                    if (e + r >= c && e < h)
                        n = c,
                        o = h,
                        a = o - e;
                    else if (e + r < c) {
                        s = c;
                        break
                    }
                }
                return {
                    len: a,
                    start: n,
                    end: o,
                    nextStart: s
                }
            }
            ,
            t
        }()
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        r.d(e, "b", function() {
            return n
        });
        var a = function() {
            function t() {
                i(this, t)
            }
            return t.isHeader = function(t, e) {
                return e + 10 <= t.length && 73 === t[e] && 68 === t[e + 1] && 51 === t[e + 2] && t[e + 3] < 255 && t[e + 4] < 255 && t[e + 6] < 128 && t[e + 7] < 128 && t[e + 8] < 128 && t[e + 9] < 128
            }
            ,
            t.isFooter = function(t, e) {
                return e + 10 <= t.length && 51 === t[e] && 68 === t[e + 1] && 73 === t[e + 2] && t[e + 3] < 255 && t[e + 4] < 255 && t[e + 6] < 128 && t[e + 7] < 128 && t[e + 8] < 128 && t[e + 9] < 128
            }
            ,
            t.getID3Data = function(e, r) {
                for (var i = r, a = 0; t.isHeader(e, r); ) {
                    a += 10;
                    a += t._readSize(e, r + 6),
                    t.isFooter(e, r + 10) && (a += 10),
                    r += a
                }
                if (a > 0)
                    return e.subarray(i, i + a)
            }
            ,
            t._readSize = function(t, e) {
                var r = 0;
                return r = (127 & t[e]) << 21,
                r |= (127 & t[e + 1]) << 14,
                r |= (127 & t[e + 2]) << 7,
                r |= 127 & t[e + 3]
            }
            ,
            t.getTimeStamp = function(e) {
                for (var r = t.getID3Frames(e), i = 0; i < r.length; i++) {
                    var a = r[i];
                    if (t.isTimeStampFrame(a))
                        return t._readTimeStamp(a)
                }
            }
            ,
            t.isTimeStampFrame = function(t) {
                return t && "PRIV" === t.key && "com.apple.streaming.transportStreamTimestamp" === t.info
            }
            ,
            t._getFrameData = function(e) {
                var r = String.fromCharCode(e[0], e[1], e[2], e[3])
                  , i = t._readSize(e, 4);
                return {
                    type: r,
                    size: i,
                    data: e.subarray(10, 10 + i)
                }
            }
            ,
            t.getID3Frames = function(e) {
                for (var r = 0, i = []; t.isHeader(e, r); ) {
                    var a = t._readSize(e, r + 6);
                    r += 10;
                    for (var n = r + a; r + 8 < n; ) {
                        var o = t._getFrameData(e.subarray(r))
                          , s = t._decodeFrame(o);
                        s && i.push(s),
                        r += o.size + 10
                    }
                    t.isFooter(e, r) && (r += 10)
                }
                return i
            }
            ,
            t._decodeFrame = function(e) {
                return "PRIV" === e.type ? t._decodePrivFrame(e) : "T" === e.type[0] ? t._decodeTextFrame(e) : "W" === e.type[0] ? t._decodeURLFrame(e) : void 0
            }
            ,
            t._readTimeStamp = function(t) {
                if (8 === t.data.byteLength) {
                    var e = new Uint8Array(t.data)
                      , r = 1 & e[3]
                      , i = (e[4] << 23) + (e[5] << 15) + (e[6] << 7) + e[7];
                    return i /= 45,
                    r && (i += 47721858.84),
                    Math.round(i)
                }
            }
            ,
            t._decodePrivFrame = function(e) {
                if (!(e.size < 2)) {
                    var r = t._utf8ArrayToStr(e.data, !0)
                      , i = new Uint8Array(e.data.subarray(r.length + 1));
                    return {
                        key: e.type,
                        info: r,
                        data: i.buffer
                    }
                }
            }
            ,
            t._decodeTextFrame = function(e) {
                if (!(e.size < 2)) {
                    if ("TXXX" === e.type) {
                        var r = 1
                          , i = t._utf8ArrayToStr(e.data.subarray(r));
                        r += i.length + 1;
                        var a = t._utf8ArrayToStr(e.data.subarray(r));
                        return {
                            key: e.type,
                            info: i,
                            data: a
                        }
                    }
                    var n = t._utf8ArrayToStr(e.data.subarray(1));
                    return {
                        key: e.type,
                        data: n
                    }
                }
            }
            ,
            t._decodeURLFrame = function(e) {
                if ("WXXX" === e.type) {
                    if (e.size < 2)
                        return;
                    var r = 1
                      , i = t._utf8ArrayToStr(e.data.subarray(r));
                    r += i.length + 1;
                    var a = t._utf8ArrayToStr(e.data.subarray(r));
                    return {
                        key: e.type,
                        info: i,
                        data: a
                    }
                }
                var n = t._utf8ArrayToStr(e.data);
                return {
                    key: e.type,
                    data: n
                }
            }
            ,
            t._utf8ArrayToStr = function(t) {
                for (var e = arguments.length > 1 && void 0 !== arguments[1] && arguments[1], r = t.length, i = void 0, a = void 0, n = void 0, o = "", s = 0; s < r; ) {
                    if (0 === (i = t[s++]) && e)
                        return o;
                    if (0 !== i && 3 !== i)
                        switch (i >> 4) {
                        case 0:
                        case 1:
                        case 2:
                        case 3:
                        case 4:
                        case 5:
                        case 6:
                        case 7:
                            o += String.fromCharCode(i);
                            break;
                        case 12:
                        case 13:
                            a = t[s++],
                            o += String.fromCharCode((31 & i) << 6 | 63 & a);
                            break;
                        case 14:
                            a = t[s++],
                            n = t[s++],
                            o += String.fromCharCode((15 & i) << 12 | (63 & a) << 6 | (63 & n) << 0)
                        }
                }
                return o
            }
            ,
            t
        }()
          , n = a._utf8ArrayToStr;
        e.a = a
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(4)
          , s = function(t) {
            function e(r) {
                i(this, e);
                for (var n = arguments.length, o = Array(n > 1 ? n - 1 : 0), s = 1; s < n; s++)
                    o[s - 1] = arguments[s];
                var l = a(this, t.call.apply(t, [this, r].concat(o)));
                return l._tickInterval = null,
                l._tickTimer = null,
                l._tickCallCount = 0,
                l._boundTick = l.tick.bind(l),
                l
            }
            return n(e, t),
            e.prototype.onHandlerDestroying = function() {
                this.clearNextTick(),
                this.clearInterval()
            }
            ,
            e.prototype.hasInterval = function() {
                return !!this._tickInterval
            }
            ,
            e.prototype.hasNextTick = function() {
                return !!this._tickTimer
            }
            ,
            e.prototype.setInterval = function(t) {
                function e(e) {
                    return t.apply(this, arguments)
                }
                return e.toString = function() {
                    return t.toString()
                }
                ,
                e
            }(function(t) {
                return !this._tickInterval && (this._tickInterval = setInterval(this._boundTick, t),
                !0)
            }),
            e.prototype.clearInterval = function(t) {
                function e() {
                    return t.apply(this, arguments)
                }
                return e.toString = function() {
                    return t.toString()
                }
                ,
                e
            }(function() {
                return !!this._tickInterval && (clearInterval(this._tickInterval),
                this._tickInterval = null,
                !0)
            }),
            e.prototype.clearNextTick = function() {
                return !!this._tickTimer && (clearTimeout(this._tickTimer),
                this._tickTimer = null,
                !0)
            }
            ,
            e.prototype.tick = function() {
                1 === ++this._tickCallCount && (this.doTick(),
                this._tickCallCount > 1 && (this.clearNextTick(),
                this._tickTimer = setTimeout(this._boundTick, 0)),
                this._tickCallCount = 0)
            }
            ,
            e.prototype.doTick = function() {}
            ,
            e
        }(o.a);
        e.a = s
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(3)
          , n = r(6)
          , o = r.n(n)
          , s = r(19)
          , l = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , u = function() {
            function t() {
                var e;
                i(this, t),
                this._url = null,
                this._byteRange = null,
                this._decryptdata = null,
                this.tagList = [],
                this.programDateTime = null,
                this.rawProgramDateTime = null,
                this._elementaryStreams = (e = {},
                e[t.ElementaryStreamTypes.AUDIO] = !1,
                e[t.ElementaryStreamTypes.VIDEO] = !1,
                e)
            }
            return t.prototype.addElementaryStream = function(t) {
                this._elementaryStreams[t] = !0
            }
            ,
            t.prototype.hasElementaryStream = function(t) {
                return !0 === this._elementaryStreams[t]
            }
            ,
            t.prototype.createInitializationVector = function(t) {
                for (var e = new Uint8Array(16), r = 12; r < 16; r++)
                    e[r] = t >> 8 * (15 - r) & 255;
                return e
            }
            ,
            t.prototype.fragmentDecryptdataFromLevelkey = function(t, e) {
                var r = t;
                return t && t.method && t.uri && !t.iv && (r = new s.a,
                r.method = t.method,
                r.baseuri = t.baseuri,
                r.reluri = t.reluri,
                r.iv = this.createInitializationVector(e)),
                r
            }
            ,
            l(t, [{
                key: "url",
                get: function() {
                    return !this._url && this.relurl && (this._url = o.a.buildAbsoluteURL(this.baseurl, this.relurl, {
                        alwaysNormalize: !0
                    })),
                    this._url
                },
                set: function(t) {
                    this._url = t
                }
            }, {
                key: "byteRange",
                get: function() {
                    if (!this._byteRange && !this.rawByteRange)
                        return [];
                    if (this._byteRange)
                        return this._byteRange;
                    var t = [];
                    if (this.rawByteRange) {
                        var e = this.rawByteRange.split("@", 2);
                        if (1 === e.length) {
                            var r = this.lastByteRangeEndOffset;
                            t[0] = r || 0
                        } else
                            t[0] = parseInt(e[1]);
                        t[1] = parseInt(e[0]) + t[0],
                        this._byteRange = t
                    }
                    return t
                }
            }, {
                key: "byteRangeStartOffset",
                get: function() {
                    return this.byteRange[0]
                }
            }, {
                key: "byteRangeEndOffset",
                get: function() {
                    return this.byteRange[1]
                }
            }, {
                key: "decryptdata",
                get: function() {
                    return this._decryptdata || (this._decryptdata = this.fragmentDecryptdataFromLevelkey(this.levelkey, this.sn)),
                    this._decryptdata
                }
            }, {
                key: "endProgramDateTime",
                get: function() {
                    if (!Object(a.a)(this.programDateTime))
                        return null;
                    var t = Object(a.a)(this.duration) ? this.duration : 0;
                    return this.programDateTime + 1e3 * t
                }
            }, {
                key: "encrypted",
                get: function() {
                    return !(!this.decryptdata || null === this.decryptdata.uri || null !== this.decryptdata.key)
                }
            }], [{
                key: "ElementaryStreamTypes",
                get: function() {
                    return {
                        AUDIO: "audio",
                        VIDEO: "video"
                    }
                }
            }]),
            t
        }();
        e.a = u
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        r.d(e, "a", function() {
            return u
        }),
        r.d(e, "b", function() {
            return d
        });
        var o = r(3)
          , s = r(4)
          , l = r(1)
          , u = {
            NOT_LOADED: "NOT_LOADED",
            APPENDING: "APPENDING",
            PARTIAL: "PARTIAL",
            OK: "OK"
        }
          , d = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, l.a.BUFFER_APPENDED, l.a.FRAG_BUFFERED, l.a.FRAG_LOADED));
                return n.bufferPadding = .2,
                n.fragments = Object.create(null),
                n.timeRanges = Object.create(null),
                n.config = r.config,
                n
            }
            return n(e, t),
            e.prototype.destroy = function() {
                this.fragments = null,
                this.timeRanges = null,
                this.config = null,
                s.a.prototype.destroy.call(this),
                t.prototype.destroy.call(this)
            }
            ,
            e.prototype.getBufferedFrag = function(t, e) {
                var r = this.fragments
                  , i = Object.keys(r).filter(function(i) {
                    var a = r[i];
                    if (a.body.type !== e)
                        return !1;
                    if (!a.buffered)
                        return !1;
                    var n = a.body;
                    return n.startPTS <= t && t <= n.endPTS
                });
                if (0 === i.length)
                    return null;
                var a = i.pop();
                return r[a].body
            }
            ,
            e.prototype.detectEvictedFragments = function(t, e) {
                var r = this
                  , i = void 0
                  , a = void 0;
                Object.keys(this.fragments).forEach(function(n) {
                    var o = r.fragments[n];
                    if (!0 === o.buffered) {
                        var s = o.range[t];
                        if (s) {
                            i = s.time;
                            for (var l = 0; l < i.length; l++)
                                if (a = i[l],
                                !1 === r.isTimeBuffered(a.startPTS, a.endPTS, e)) {
                                    r.removeFragment(o.body);
                                    break
                                }
                        }
                    }
                })
            }
            ,
            e.prototype.detectPartialFragments = function(t) {
                var e = this
                  , r = this.getFragmentKey(t)
                  , i = this.fragments[r];
                i && (i.buffered = !0,
                Object.keys(this.timeRanges).forEach(function(r) {
                    if (t.hasElementaryStream(r)) {
                        var a = e.timeRanges[r];
                        i.range[r] = e.getBufferedTimes(t.startPTS, t.endPTS, a)
                    }
                }))
            }
            ,
            e.prototype.getBufferedTimes = function(t, e, r) {
                for (var i = [], a = void 0, n = void 0, o = !1, s = 0; s < r.length; s++) {
                    if (a = r.start(s) - this.bufferPadding,
                    n = r.end(s) + this.bufferPadding,
                    t >= a && e <= n) {
                        i.push({
                            startPTS: Math.max(t, r.start(s)),
                            endPTS: Math.min(e, r.end(s))
                        });
                        break
                    }
                    if (t < n && e > a)
                        i.push({
                            startPTS: Math.max(t, r.start(s)),
                            endPTS: Math.min(e, r.end(s))
                        }),
                        o = !0;
                    else if (e <= a)
                        break
                }
                return {
                    time: i,
                    partial: o
                }
            }
            ,
            e.prototype.getFragmentKey = function(t) {
                return t.type + "_" + t.level + "_" + t.urlId + "_" + t.sn
            }
            ,
            e.prototype.getPartialFragment = function(t) {
                var e = this
                  , r = void 0
                  , i = void 0
                  , a = void 0
                  , n = null
                  , o = 0;
                return Object.keys(this.fragments).forEach(function(s) {
                    var l = e.fragments[s];
                    e.isPartial(l) && (i = l.body.startPTS - e.bufferPadding,
                    a = l.body.endPTS + e.bufferPadding,
                    t >= i && t <= a && (r = Math.min(t - i, a - t),
                    o <= r && (n = l.body,
                    o = r)))
                }),
                n
            }
            ,
            e.prototype.getState = function(t) {
                var e = this.getFragmentKey(t)
                  , r = this.fragments[e]
                  , i = u.NOT_LOADED;
                return void 0 !== r && (i = r.buffered ? !0 === this.isPartial(r) ? u.PARTIAL : u.OK : u.APPENDING),
                i
            }
            ,
            e.prototype.isPartial = function(t) {
                return !0 === t.buffered && (void 0 !== t.range.video && !0 === t.range.video.partial || void 0 !== t.range.audio && !0 === t.range.audio.partial)
            }
            ,
            e.prototype.isTimeBuffered = function(t, e, r) {
                for (var i = void 0, a = void 0, n = 0; n < r.length; n++) {
                    if (i = r.start(n) - this.bufferPadding,
                    a = r.end(n) + this.bufferPadding,
                    t >= i && e <= a)
                        return !0;
                    if (e <= i)
                        return !1
                }
                return !1
            }
            ,
            e.prototype.onFragLoaded = function(t) {
                var e = t.frag;
                Object(o.a)(e.sn) && !e.bitrateTest && (this.fragments[this.getFragmentKey(e)] = {
                    body: e,
                    range: Object.create(null),
                    buffered: !1
                })
            }
            ,
            e.prototype.onBufferAppended = function(t) {
                var e = this;
                this.timeRanges = t.timeRanges,
                Object.keys(this.timeRanges).forEach(function(t) {
                    var r = e.timeRanges[t];
                    e.detectEvictedFragments(t, r)
                })
            }
            ,
            e.prototype.onFragBuffered = function(t) {
                this.detectPartialFragments(t.frag)
            }
            ,
            e.prototype.hasFragment = function(t) {
                var e = this.getFragmentKey(t);
                return void 0 !== this.fragments[e]
            }
            ,
            e.prototype.removeFragment = function(t) {
                var e = this.getFragmentKey(t);
                delete this.fragments[e]
            }
            ,
            e.prototype.removeAllFragments = function() {
                this.fragments = Object.create(null)
            }
            ,
            e
        }(s.a)
    }
    , function(t, e) {
        function r() {
            this._events = this._events || {},
            this._maxListeners = this._maxListeners || void 0
        }
        function i(t) {
            return "function" == typeof t
        }
        function a(t) {
            return "number" == typeof t
        }
        function n(t) {
            return "object" == typeof t && null !== t
        }
        function o(t) {
            return void 0 === t
        }
        t.exports = r,
        r.EventEmitter = r,
        r.prototype._events = void 0,
        r.prototype._maxListeners = void 0,
        r.defaultMaxListeners = 10,
        r.prototype.setMaxListeners = function(t) {
            if (!a(t) || t < 0 || isNaN(t))
                throw TypeError("n must be a positive number");
            return this._maxListeners = t,
            this
        }
        ,
        r.prototype.emit = function(t) {
            var e, r, a, s, l, u;
            if (this._events || (this._events = {}),
            "error" === t && (!this._events.error || n(this._events.error) && !this._events.error.length)) {
                if ((e = arguments[1])instanceof Error)
                    throw e;
                var d = new Error('Uncaught, unspecified "error" event. (' + e + ")");
                throw d.context = e,
                d
            }
            if (r = this._events[t],
            o(r))
                return !1;
            if (i(r))
                switch (arguments.length) {
                case 1:
                    r.call(this);
                    break;
                case 2:
                    r.call(this, arguments[1]);
                    break;
                case 3:
                    r.call(this, arguments[1], arguments[2]);
                    break;
                default:
                    s = Array.prototype.slice.call(arguments, 1),
                    r.apply(this, s)
                }
            else if (n(r))
                for (s = Array.prototype.slice.call(arguments, 1),
                u = r.slice(),
                a = u.length,
                l = 0; l < a; l++)
                    u[l].apply(this, s);
            return !0
        }
        ,
        r.prototype.addListener = function(t, e) {
            var a;
            if (!i(e))
                throw TypeError("listener must be a function");
            return this._events || (this._events = {}),
            this._events.newListener && this.emit("newListener", t, i(e.listener) ? e.listener : e),
            this._events[t] ? n(this._events[t]) ? this._events[t].push(e) : this._events[t] = [this._events[t], e] : this._events[t] = e,
            n(this._events[t]) && !this._events[t].warned && (a = o(this._maxListeners) ? r.defaultMaxListeners : this._maxListeners) && a > 0 && this._events[t].length > a && (this._events[t].warned = !0,
            console.error("(node) warning: possible EventEmitter memory leak detected. %d listeners added. Use emitter.setMaxListeners() to increase limit.", this._events[t].length),
            "function" == typeof console.trace && console.trace()),
            this
        }
        ,
        r.prototype.on = r.prototype.addListener,
        r.prototype.once = function(t, e) {
            function r() {
                this.removeListener(t, r),
                a || (a = !0,
                e.apply(this, arguments))
            }
            if (!i(e))
                throw TypeError("listener must be a function");
            var a = !1;
            return r.listener = e,
            this.on(t, r),
            this
        }
        ,
        r.prototype.removeListener = function(t, e) {
            var r, a, o, s;
            if (!i(e))
                throw TypeError("listener must be a function");
            if (!this._events || !this._events[t])
                return this;
            if (r = this._events[t],
            o = r.length,
            a = -1,
            r === e || i(r.listener) && r.listener === e)
                delete this._events[t],
                this._events.removeListener && this.emit("removeListener", t, e);
            else if (n(r)) {
                for (s = o; s-- > 0; )
                    if (r[s] === e || r[s].listener && r[s].listener === e) {
                        a = s;
                        break
                    }
                if (a < 0)
                    return this;
                1 === r.length ? (r.length = 0,
                delete this._events[t]) : r.splice(a, 1),
                this._events.removeListener && this.emit("removeListener", t, e)
            }
            return this
        }
        ,
        r.prototype.removeAllListeners = function(t) {
            var e, r;
            if (!this._events)
                return this;
            if (!this._events.removeListener)
                return 0 === arguments.length ? this._events = {} : this._events[t] && delete this._events[t],
                this;
            if (0 === arguments.length) {
                for (e in this._events)
                    "removeListener" !== e && this.removeAllListeners(e);
                return this.removeAllListeners("removeListener"),
                this._events = {},
                this
            }
            if (r = this._events[t],
            i(r))
                this.removeListener(t, r);
            else if (r)
                for (; r.length; )
                    this.removeListener(t, r[r.length - 1]);
            return delete this._events[t],
            this
        }
        ,
        r.prototype.listeners = function(t) {
            return this._events && this._events[t] ? i(this._events[t]) ? [this._events[t]] : this._events[t].slice() : []
        }
        ,
        r.prototype.listenerCount = function(t) {
            if (this._events) {
                var e = this._events[t];
                if (i(e))
                    return 1;
                if (e)
                    return e.length
            }
            return 0
        }
        ,
        r.listenerCount = function(t, e) {
            return t.listenerCount(e)
        }
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(37)
          , n = r(38)
          , o = r(39)
          , s = r(2)
          , l = r(0)
          , u = r(1)
          , d = r(5)
          , c = Object(d.a)()
          , h = function() {
            function t(e, r) {
                var a = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : {}
                  , n = a.removePKCS7Padding
                  , o = void 0 === n || n;
                if (i(this, t),
                this.logEnabled = !0,
                this.observer = e,
                this.config = r,
                this.removePKCS7Padding = o,
                o)
                    try {
                        var s = c.crypto;
                        s && (this.subtle = s.subtle || s.webkitSubtle)
                    } catch (t) {}
                this.disableWebCrypto = !this.subtle
            }
            return t.prototype.isSync = function() {
                return this.disableWebCrypto && this.config.enableSoftwareAES
            }
            ,
            t.prototype.decrypt = function(t, e, r, i) {
                var s = this;
                if (this.disableWebCrypto && this.config.enableSoftwareAES) {
                    this.logEnabled && (l.b.log("JS AES decrypt"),
                    this.logEnabled = !1);
                    var u = this.decryptor;
                    u || (this.decryptor = u = new o.a),
                    u.expandKey(e),
                    i(u.decrypt(t, 0, r, this.removePKCS7Padding))
                } else {
                    this.logEnabled && (l.b.log("WebCrypto AES decrypt"),
                    this.logEnabled = !1);
                    var d = this.subtle;
                    this.key !== e && (this.key = e,
                    this.fastAesKey = new n.a(d,e)),
                    this.fastAesKey.expandKey().then(function(n) {
                        new a.a(d,r).decrypt(t, n).catch(function(a) {
                            s.onWebCryptoError(a, t, e, r, i)
                        }).then(function(t) {
                            i(t)
                        })
                    }).catch(function(a) {
                        s.onWebCryptoError(a, t, e, r, i)
                    })
                }
            }
            ,
            t.prototype.onWebCryptoError = function(t, e, r, i, a) {
                this.config.enableSoftwareAES ? (l.b.log("WebCrypto Error, disable WebCrypto API"),
                this.disableWebCrypto = !0,
                this.logEnabled = !0,
                this.decrypt(e, r, i, a)) : (l.b.error("decrypting error : " + t.message),
                this.observer.trigger(u.a.ERROR, {
                    type: s.b.MEDIA_ERROR,
                    details: s.a.FRAG_DECRYPT_ERROR,
                    fatal: !0,
                    reason: t.message
                }))
            }
            ,
            t.prototype.destroy = function() {
                var t = this.decryptor;
                t && (t.destroy(),
                this.decryptor = void 0)
            }
            ,
            t
        }();
        e.a = h
    }
    , function(t, e, r) {
        "use strict";
        function i() {
            if ("undefined" != typeof window)
                return window.MediaSource || window.WebKitMediaSource
        }
        e.a = i
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e, r) {
            switch (e) {
            case "audio":
                t.audioGroupIds || (t.audioGroupIds = []),
                t.audioGroupIds.push(r);
                break;
            case "text":
                t.textGroupIds || (t.textGroupIds = []),
                t.textGroupIds.push(r)
            }
        }
        function a(t, e, r) {
            var i = t[e]
              , a = t[r]
              , n = a.startPTS;
            Object(s.a)(n) ? r > e ? (i.duration = n - i.start,
            i.duration < 0 && l.b.warn("negative duration computed for frag " + i.sn + ",level " + i.level + ", there should be some duration drift between playlist and fragment!")) : (a.duration = i.start - n,
            a.duration < 0 && l.b.warn("negative duration computed for frag " + a.sn + ",level " + a.level + ", there should be some duration drift between playlist and fragment!")) : a.start = r > e ? i.start + i.duration : Math.max(i.start - a.duration, 0)
        }
        function n(t, e, r, i, n, o) {
            var l = r;
            if (Object(s.a)(e.startPTS)) {
                var u = Math.abs(e.startPTS - r);
                Object(s.a)(e.deltaPTS) ? e.deltaPTS = Math.max(u, e.deltaPTS) : e.deltaPTS = u,
                l = Math.max(r, e.startPTS),
                r = Math.min(r, e.startPTS),
                i = Math.max(i, e.endPTS),
                n = Math.min(n, e.startDTS),
                o = Math.max(o, e.endDTS)
            }
            var d = r - e.start;
            e.start = e.startPTS = r,
            e.maxStartPTS = l,
            e.endPTS = i,
            e.startDTS = n,
            e.endDTS = o,
            e.duration = i - r;
            var c = e.sn;
            if (!t || c < t.startSN || c > t.endSN)
                return 0;
            var h = void 0
              , f = void 0
              , p = void 0;
            for (h = c - t.startSN,
            f = t.fragments,
            f[h] = e,
            p = h; p > 0; p--)
                a(f, p, p - 1);
            for (p = h; p < f.length - 1; p++)
                a(f, p, p + 1);
            return t.PTSKnown = !0,
            d
        }
        function o(t, e) {
            var r = Math.max(t.startSN, e.startSN) - e.startSN
              , i = Math.min(t.endSN, e.endSN) - e.startSN
              , a = e.startSN - t.startSN
              , o = t.fragments
              , u = e.fragments
              , d = 0
              , c = void 0;
            if (e.initSegment && t.initSegment && (e.initSegment = t.initSegment),
            i < r)
                return void (e.PTSKnown = !1);
            for (var h = r; h <= i; h++) {
                var f = o[a + h]
                  , p = u[h];
                p && f && (d = f.cc - p.cc,
                Object(s.a)(f.startPTS) && (p.start = p.startPTS = f.startPTS,
                p.endPTS = f.endPTS,
                p.duration = f.duration,
                p.backtracked = f.backtracked,
                p.dropped = f.dropped,
                c = p))
            }
            if (d)
                for (l.b.log("discontinuity sliding from playlist, take drift into account"),
                h = 0; h < u.length; h++)
                    u[h].cc += d;
            if (c)
                n(e, c, c.startPTS, c.endPTS, c.startDTS, c.endDTS);
            else if (a >= 0 && a < o.length) {
                var g = o[a].start;
                for (h = 0; h < u.length; h++)
                    u[h].start += g
            }
            e.PTSKnown = t.PTSKnown
        }
        e.a = i,
        e.c = n,
        e.b = o;
        var s = r(3)
          , l = r(0)
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(3)
          , s = r(1)
          , l = r(4)
          , u = r(2)
          , d = r(0)
          , c = r(18)
          , h = r(30)
          , f = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , p = window
          , g = p.performance
          , v = {
            MANIFEST: "manifest",
            LEVEL: "level",
            AUDIO_TRACK: "audioTrack",
            SUBTITLE_TRACK: "subtitleTrack"
        }
          , y = {
            MAIN: "main",
            AUDIO: "audio",
            SUBTITLE: "subtitle"
        }
          , m = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, s.a.MANIFEST_LOADING, s.a.LEVEL_LOADING, s.a.AUDIO_TRACK_LOADING, s.a.SUBTITLE_TRACK_LOADING));
                return n.loaders = {},
                n
            }
            return n(e, t),
            e.canHaveQualityLevels = function(t) {
                return t !== v.AUDIO_TRACK && t !== v.SUBTITLE_TRACK
            }
            ,
            e.mapContextToLevelType = function(t) {
                switch (t.type) {
                case v.AUDIO_TRACK:
                    return y.AUDIO;
                case v.SUBTITLE_TRACK:
                    return y.SUBTITLE;
                default:
                    return y.MAIN
                }
            }
            ,
            e.getResponseUrl = function(t, e) {
                var r = t.url;
                return void 0 !== r && 0 !== r.indexOf("data:") || (r = e.url),
                r
            }
            ,
            e.prototype.createInternalLoader = function(t) {
                var e = this.hls.config
                  , r = e.pLoader
                  , i = e.loader
                  , a = r || i
                  , n = new a(e);
                return t.loader = n,
                this.loaders[t.type] = n,
                n
            }
            ,
            e.prototype.getInternalLoader = function(t) {
                return this.loaders[t.type]
            }
            ,
            e.prototype.resetInternalLoader = function(t) {
                this.loaders[t] && delete this.loaders[t]
            }
            ,
            e.prototype.destroyInternalLoaders = function() {
                for (var t in this.loaders) {
                    var e = this.loaders[t];
                    e && e.destroy(),
                    this.resetInternalLoader(t)
                }
            }
            ,
            e.prototype.destroy = function() {
                this.destroyInternalLoaders(),
                t.prototype.destroy.call(this)
            }
            ,
            e.prototype.onManifestLoading = function(t) {
                this.load(t.url, {
                    type: v.MANIFEST,
                    level: 0,
                    id: null
                })
            }
            ,
            e.prototype.onLevelLoading = function(t) {
                this.load(t.url, {
                    type: v.LEVEL,
                    level: t.level,
                    id: t.id
                })
            }
            ,
            e.prototype.onAudioTrackLoading = function(t) {
                this.load(t.url, {
                    type: v.AUDIO_TRACK,
                    level: null,
                    id: t.id
                })
            }
            ,
            e.prototype.onSubtitleTrackLoading = function(t) {
                this.load(t.url, {
                    type: v.SUBTITLE_TRACK,
                    level: null,
                    id: t.id
                })
            }
            ,
            e.prototype.load = function(t, e) {
                var r = this.hls.config;
                d.b.debug("Loading playlist of type " + e.type + ", level: " + e.level + ", id: " + e.id);
                var i = this.getInternalLoader(e);
                if (i) {
                    var a = i.context;
                    if (a && a.url === t)
                        return d.b.trace("playlist request ongoing"),
                        !1;
                    d.b.warn("aborting previous loader for type: " + e.type),
                    i.abort()
                }
                var n = void 0
                  , o = void 0
                  , s = void 0
                  , l = void 0;
                switch (e.type) {
                case v.MANIFEST:
                    n = r.manifestLoadingMaxRetry,
                    o = r.manifestLoadingTimeOut,
                    s = r.manifestLoadingRetryDelay,
                    l = r.manifestLoadingMaxRetryTimeout;
                    break;
                case v.LEVEL:
                    n = 0,
                    o = r.levelLoadingTimeOut;
                    break;
                default:
                    n = r.levelLoadingMaxRetry,
                    o = r.levelLoadingTimeOut,
                    s = r.levelLoadingRetryDelay,
                    l = r.levelLoadingMaxRetryTimeout
                }
                i = this.createInternalLoader(e),
                e.url = t,
                e.responseType = e.responseType || "";
                var u = {
                    timeout: o,
                    maxRetry: n,
                    retryDelay: s,
                    maxRetryDelay: l
                }
                  , c = {
                    onSuccess: this.loadsuccess.bind(this),
                    onError: this.loaderror.bind(this),
                    onTimeout: this.loadtimeout.bind(this)
                };
                return d.b.debug("Calling internal loader delegate for URL: " + t),
                i.load(e, u, c),
                !0
            }
            ,
            e.prototype.loadsuccess = function(t, e, r) {
                var i = arguments.length > 3 && void 0 !== arguments[3] ? arguments[3] : null;
                if (r.isSidxRequest)
                    return this._handleSidxRequest(t, r),
                    void this._handlePlaylistLoaded(t, e, r, i);
                this.resetInternalLoader(r.type);
                var a = t.data;
                if (e.tload = g.now(),
                0 !== a.indexOf("#EXTM3U"))
                    return void this._handleManifestParsingError(t, r, "no EXTM3U delimiter", i);
                a.indexOf("#EXTINF:") > 0 || a.indexOf("#EXT-X-TARGETDURATION:") > 0 ? this._handleTrackOrLevelPlaylist(t, e, r, i) : this._handleMasterPlaylist(t, e, r, i)
            }
            ,
            e.prototype.loaderror = function(t, e) {
                var r = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : null;
                this._handleNetworkError(e, r)
            }
            ,
            e.prototype.loadtimeout = function(t, e) {
                var r = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : null;
                this._handleNetworkError(e, r, !0)
            }
            ,
            e.prototype._handleMasterPlaylist = function(t, r, i, a) {
                var n = this.hls
                  , o = t.data
                  , l = e.getResponseUrl(t, i)
                  , u = h.a.parseMasterPlaylist(o, l);
                if (!u.length)
                    return void this._handleManifestParsingError(t, i, "no level found in manifest", a);
                var c = u.map(function(t) {
                    return {
                        id: t.attrs.AUDIO,
                        codec: t.audioCodec
                    }
                })
                  , f = h.a.parseMasterPlaylistMedia(o, l, "AUDIO", c)
                  , p = h.a.parseMasterPlaylistMedia(o, l, "SUBTITLES");
                if (f.length) {
                    var g = !1;
                    f.forEach(function(t) {
                        t.url || (g = !0)
                    }),
                    !1 === g && u[0].audioCodec && !u[0].attrs.AUDIO && (d.b.log("audio codec signaled in quality level, but no embedded audio track signaled, create one"),
                    f.unshift({
                        type: "main",
                        name: "main"
                    }))
                }
                n.trigger(s.a.MANIFEST_LOADED, {
                    levels: u,
                    audioTracks: f,
                    subtitles: p,
                    url: l,
                    stats: r,
                    networkDetails: a
                })
            }
            ,
            e.prototype._handleTrackOrLevelPlaylist = function(t, r, i, a) {
                var n = this.hls
                  , l = i.id
                  , u = i.level
                  , d = i.type
                  , c = e.getResponseUrl(t, i)
                  , f = Object(o.a)(l) ? l : 0
                  , p = Object(o.a)(u) ? u : f
                  , y = e.mapContextToLevelType(i)
                  , m = h.a.parseLevelPlaylist(t.data, c, p, y, f);
                if (m.tload = r.tload,
                d === v.MANIFEST) {
                    var b = {
                        url: c,
                        details: m
                    };
                    n.trigger(s.a.MANIFEST_LOADED, {
                        levels: [b],
                        audioTracks: [],
                        url: c,
                        stats: r,
                        networkDetails: a
                    })
                }
                if (r.tparsed = g.now(),
                m.needSidxRanges) {
                    var E = m.initSegment.url;
                    return void this.load(E, {
                        isSidxRequest: !0,
                        type: d,
                        level: u,
                        levelDetails: m,
                        id: l,
                        rangeStart: 0,
                        rangeEnd: 2048,
                        responseType: "arraybuffer"
                    })
                }
                i.levelDetails = m,
                this._handlePlaylistLoaded(t, r, i, a)
            }
            ,
            e.prototype._handleSidxRequest = function(t, e) {
                var r = c.a.parseSegmentIndex(new Uint8Array(t.data));
                r.references.forEach(function(t, r) {
                    var i = t.info
                      , a = e.levelDetails.fragments[r];
                    0 === a.byteRange.length && (a.rawByteRange = String(1 + i.end - i.start) + "@" + String(i.start))
                }),
                e.levelDetails.initSegment.rawByteRange = String(r.moovEndOffset) + "@0"
            }
            ,
            e.prototype._handleManifestParsingError = function(t, e, r, i) {
                this.hls.trigger(s.a.ERROR, {
                    type: u.b.NETWORK_ERROR,
                    details: u.a.MANIFEST_PARSING_ERROR,
                    fatal: !0,
                    url: t.url,
                    reason: r,
                    networkDetails: i
                })
            }
            ,
            e.prototype._handleNetworkError = function(t, e) {
                var r = arguments.length > 2 && void 0 !== arguments[2] && arguments[2];
                d.b.info("A network error occured while loading a " + t.type + "-type playlist");
                var i = void 0
                  , a = void 0
                  , n = this.getInternalLoader(t);
                switch (t.type) {
                case v.MANIFEST:
                    i = r ? u.a.MANIFEST_LOAD_TIMEOUT : u.a.MANIFEST_LOAD_ERROR,
                    a = !0;
                    break;
                case v.LEVEL:
                    i = r ? u.a.LEVEL_LOAD_TIMEOUT : u.a.LEVEL_LOAD_ERROR,
                    a = !1;
                    break;
                case v.AUDIO_TRACK:
                    i = r ? u.a.AUDIO_TRACK_LOAD_TIMEOUT : u.a.AUDIO_TRACK_LOAD_ERROR,
                    a = !1;
                    break;
                default:
                    a = !1
                }
                n && (n.abort(),
                this.resetInternalLoader(t.type)),
                this.hls.trigger(s.a.ERROR, {
                    type: u.b.NETWORK_ERROR,
                    details: i,
                    fatal: a,
                    url: n.url,
                    loader: n,
                    context: t,
                    networkDetails: e
                })
            }
            ,
            e.prototype._handlePlaylistLoaded = function(t, r, i, a) {
                var n = i.type
                  , o = i.level
                  , l = i.id
                  , u = i.levelDetails;
                if (!u.targetduration)
                    return void this._handleManifestParsingError(t, i, "invalid target duration", a);
                if (e.canHaveQualityLevels(i.type))
                    this.hls.trigger(s.a.LEVEL_LOADED, {
                        details: u,
                        level: o || 0,
                        id: l || 0,
                        stats: r,
                        networkDetails: a
                    });
                else
                    switch (n) {
                    case v.AUDIO_TRACK:
                        this.hls.trigger(s.a.AUDIO_TRACK_LOADED, {
                            details: u,
                            id: l,
                            stats: r,
                            networkDetails: a
                        });
                        break;
                    case v.SUBTITLE_TRACK:
                        this.hls.trigger(s.a.SUBTITLE_TRACK_LOADED, {
                            details: u,
                            id: l,
                            stats: r,
                            networkDetails: a
                        })
                    }
            }
            ,
            f(e, null, [{
                key: "ContextType",
                get: function() {
                    return v
                }
            }, {
                key: "LevelType",
                get: function() {
                    return y
                }
            }]),
            e
        }(l.a);
        e.a = m
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(0)
          , n = r(1)
          , o = Math.pow(2, 32) - 1
          , s = function() {
            function t(e, r) {
                i(this, t),
                this.observer = e,
                this.remuxer = r
            }
            return t.prototype.resetTimeStamp = function(t) {
                this.initPTS = t
            }
            ,
            t.prototype.resetInitSegment = function(e, r, i, a) {
                if (e && e.byteLength) {
                    var o = this.initData = t.parseInitSegment(e);
                    null == r && (r = "mp4a.40.5"),
                    null == i && (i = "avc1.42e01e");
                    var s = {};
                    o.audio && o.video ? s.audiovideo = {
                        container: "video/mp4",
                        codec: r + "," + i,
                        initSegment: a ? e : null
                    } : (o.audio && (s.audio = {
                        container: "audio/mp4",
                        codec: r,
                        initSegment: a ? e : null
                    }),
                    o.video && (s.video = {
                        container: "video/mp4",
                        codec: i,
                        initSegment: a ? e : null
                    })),
                    this.observer.trigger(n.a.FRAG_PARSING_INIT_SEGMENT, {
                        tracks: s
                    })
                } else
                    r && (this.audioCodec = r),
                    i && (this.videoCodec = i)
            }
            ,
            t.probe = function(e) {
                return t.findBox({
                    data: e,
                    start: 0,
                    end: Math.min(e.length, 16384)
                }, ["moof"]).length > 0
            }
            ,
            t.bin2str = function(t) {
                return String.fromCharCode.apply(null, t)
            }
            ,
            t.readUint16 = function(t, e) {
                t.data && (e += t.start,
                t = t.data);
                var r = t[e] << 8 | t[e + 1];
                return r < 0 ? 65536 + r : r
            }
            ,
            t.readUint32 = function(t, e) {
                t.data && (e += t.start,
                t = t.data);
                var r = t[e] << 24 | t[e + 1] << 16 | t[e + 2] << 8 | t[e + 3];
                return r < 0 ? 4294967296 + r : r
            }
            ,
            t.writeUint32 = function(t, e, r) {
                t.data && (e += t.start,
                t = t.data),
                t[e] = r >> 24,
                t[e + 1] = r >> 16 & 255,
                t[e + 2] = r >> 8 & 255,
                t[e + 3] = 255 & r
            }
            ,
            t.findBox = function(e, r) {
                var i = []
                  , a = void 0
                  , n = void 0
                  , o = void 0
                  , s = void 0
                  , l = void 0
                  , u = void 0
                  , d = void 0;
                if (e.data ? (u = e.start,
                s = e.end,
                e = e.data) : (u = 0,
                s = e.byteLength),
                !r.length)
                    return null;
                for (a = u; a < s; )
                    n = t.readUint32(e, a),
                    o = t.bin2str(e.subarray(a + 4, a + 8)),
                    d = n > 1 ? a + n : s,
                    o === r[0] && (1 === r.length ? i.push({
                        data: e,
                        start: a + 8,
                        end: d
                    }) : (l = t.findBox({
                        data: e,
                        start: a + 8,
                        end: d
                    }, r.slice(1)),
                    l.length && (i = i.concat(l)))),
                    a = d;
                return i
            }
            ,
            t.parseSegmentIndex = function(e) {
                var r = t.findBox(e, ["moov"])[0]
                  , i = r ? r.end : null
                  , a = 0
                  , n = t.findBox(e, ["sidx"])
                  , o = void 0;
                if (!n || !n[0])
                    return null;
                o = [],
                n = n[0];
                var s = n.data[0];
                a = 0 === s ? 8 : 16;
                var l = t.readUint32(n, a);
                a += 4;
                a += 0 === s ? 8 : 16,
                a += 2;
                var u = n.end + 0
                  , d = t.readUint16(n, a);
                a += 2;
                for (var c = 0; c < d; c++) {
                    var h = a
                      , f = t.readUint32(n, h);
                    h += 4;
                    var p = 2147483647 & f;
                    if (1 === (2147483648 & f) >>> 31)
                        return void console.warn("SIDX has hierarchical references (not supported)");
                    var g = t.readUint32(n, h);
                    h += 4,
                    o.push({
                        referenceSize: p,
                        subsegmentDuration: g,
                        info: {
                            duration: g / l,
                            start: u,
                            end: u + p - 1
                        }
                    }),
                    u += p,
                    h += 4,
                    a = h
                }
                return {
                    earliestPresentationTime: 0,
                    timescale: l,
                    version: s,
                    referencesCount: d,
                    references: o,
                    moovEndOffset: i
                }
            }
            ,
            t.parseInitSegment = function(e) {
                var r = [];
                return t.findBox(e, ["moov", "trak"]).forEach(function(e) {
                    var i = t.findBox(e, ["tkhd"])[0];
                    if (i) {
                        var n = i.data[i.start]
                          , o = 0 === n ? 12 : 20
                          , s = t.readUint32(i, o)
                          , l = t.findBox(e, ["mdia", "mdhd"])[0];
                        if (l) {
                            n = l.data[l.start],
                            o = 0 === n ? 12 : 20;
                            var u = t.readUint32(l, o)
                              , d = t.findBox(e, ["mdia", "hdlr"])[0];
                            if (d) {
                                var c = t.bin2str(d.data.subarray(d.start + 8, d.start + 12))
                                  , h = {
                                    soun: "audio",
                                    vide: "video"
                                }[c];
                                if (h) {
                                    var f = t.findBox(e, ["mdia", "minf", "stbl", "stsd"]);
                                    if (f.length) {
                                        f = f[0];
                                        var p = t.bin2str(f.data.subarray(f.start + 12, f.start + 16));
                                        a.b.log("MP4Demuxer:" + h + ":" + p + " found")
                                    }
                                    r[s] = {
                                        timescale: u,
                                        type: h
                                    },
                                    r[h] = {
                                        timescale: u,
                                        id: s
                                    }
                                }
                            }
                        }
                    }
                }),
                r
            }
            ,
            t.getStartDTS = function(e, r) {
                var i = void 0
                  , a = void 0
                  , n = void 0;
                return i = t.findBox(r, ["moof", "traf"]),
                a = [].concat.apply([], i.map(function(r) {
                    return t.findBox(r, ["tfhd"]).map(function(i) {
                        var a = void 0
                          , n = void 0;
                        return a = t.readUint32(i, 4),
                        n = e[a].timescale || 9e4,
                        t.findBox(r, ["tfdt"]).map(function(e) {
                            var r = void 0
                              , i = void 0;
                            return r = e.data[e.start],
                            i = t.readUint32(e, 4),
                            1 === r && (i *= Math.pow(2, 32),
                            i += t.readUint32(e, 8)),
                            i
                        })[0] / n
                    })
                })),
                n = Math.min.apply(null, a),
                isFinite(n) ? n : 0
            }
            ,
            t.offsetStartDTS = function(e, r, i) {
                t.findBox(r, ["moof", "traf"]).map(function(r) {
                    return t.findBox(r, ["tfhd"]).map(function(a) {
                        var n = t.readUint32(a, 4)
                          , s = e[n].timescale || 9e4;
                        t.findBox(r, ["tfdt"]).map(function(e) {
                            var r = e.data[e.start]
                              , a = t.readUint32(e, 4);
                            if (0 === r)
                                t.writeUint32(e, 4, a - i * s);
                            else {
                                a *= Math.pow(2, 32),
                                a += t.readUint32(e, 8),
                                a -= i * s,
                                a = Math.max(a, 0);
                                var n = Math.floor(a / (o + 1))
                                  , l = Math.floor(a % (o + 1));
                                t.writeUint32(e, 4, n),
                                t.writeUint32(e, 8, l)
                            }
                        })
                    })
                })
            }
            ,
            t.prototype.append = function(e, r, i, a) {
                var o = this.initData;
                o || (this.resetInitSegment(e, this.audioCodec, this.videoCodec, !1),
                o = this.initData);
                var s = void 0
                  , l = this.initPTS;
                if (void 0 === l) {
                    var u = t.getStartDTS(o, e);
                    this.initPTS = l = u - r,
                    this.observer.trigger(n.a.INIT_PTS_FOUND, {
                        initPTS: l
                    })
                }
                t.offsetStartDTS(o, e, l),
                s = t.getStartDTS(o, e),
                this.remuxer.remux(o.audio, o.video, null, null, s, i, a, e)
            }
            ,
            t.prototype.destroy = function() {}
            ,
            t
        }();
        e.a = s
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(6)
          , n = r.n(a)
          , o = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , s = function() {
            function t() {
                i(this, t),
                this.method = null,
                this.key = null,
                this.iv = null,
                this._uri = null
            }
            return o(t, [{
                key: "uri",
                get: function() {
                    return !this._uri && this.reluri && (this._uri = n.a.buildAbsoluteURL(this.baseuri, this.reluri, {
                        alwaysNormalize: !0
                    })),
                    this._uri
                }
            }]),
            t
        }();
        e.a = s
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            var r = n[e];
            return !!r && !0 === r[t.slice(0, 4)]
        }
        function a(t, e) {
            return window.MediaSource.isTypeSupported((e || "video") + '/mp4;codecs="' + t + '"')
        }
        r.d(e, "b", function() {
            return i
        }),
        r.d(e, "a", function() {
            return a
        });
        var n = {
            audio: {
                a3ds: !0,
                "ac-3": !0,
                "ac-4": !0,
                alac: !0,
                alaw: !0,
                dra1: !0,
                "dts+": !0,
                "dts-": !0,
                dtsc: !0,
                dtse: !0,
                dtsh: !0,
                "ec-3": !0,
                enca: !0,
                g719: !0,
                g726: !0,
                m4ae: !0,
                mha1: !0,
                mha2: !0,
                mhm1: !0,
                mhm2: !0,
                mlpa: !0,
                mp4a: !0,
                "raw ": !0,
                Opus: !0,
                samr: !0,
                sawb: !0,
                sawp: !0,
                sevc: !0,
                sqcp: !0,
                ssmv: !0,
                twos: !0,
                ulaw: !0
            },
            video: {
                avc1: !0,
                avc2: !0,
                avc3: !0,
                avc4: !0,
                avcp: !0,
                drac: !0,
                dvav: !0,
                dvhe: !0,
                encv: !0,
                hev1: !0,
                hvc1: !0,
                mjp2: !0,
                mp4v: !0,
                mvc1: !0,
                mvc2: !0,
                mvc3: !0,
                mvc4: !0,
                resv: !0,
                rv60: !0,
                s263: !0,
                svc1: !0,
                svc2: !0,
                "vc-1": !0,
                vp08: !0,
                vp09: !0
            }
        }
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(3)
          , n = r(13)
          , o = r.n(n)
          , s = r(36)
          , l = r.n(s)
          , u = r(1)
          , d = r(22)
          , c = r(0)
          , h = r(2)
          , f = r(15)
          , p = r(5)
          , g = Object(p.a)()
          , v = Object(f.a)()
          , y = function() {
            function t(e, r) {
                i(this, t),
                this.hls = e,
                this.id = r;
                var a = this.observer = new o.a
                  , n = e.config;
                a.trigger = function(t) {
                    for (var e = arguments.length, r = Array(e > 1 ? e - 1 : 0), i = 1; i < e; i++)
                        r[i - 1] = arguments[i];
                    a.emit.apply(a, [t, t].concat(r))
                }
                ,
                a.off = function(t) {
                    for (var e = arguments.length, r = Array(e > 1 ? e - 1 : 0), i = 1; i < e; i++)
                        r[i - 1] = arguments[i];
                    a.removeListener.apply(a, [t].concat(r))
                }
                ;
                var s = function(t, r) {
                    r = r || {},
                    r.frag = this.frag,
                    r.id = this.id,
                    e.trigger(t, r)
                }
                .bind(this);
                a.on(u.a.FRAG_DECRYPTED, s),
                a.on(u.a.FRAG_PARSING_INIT_SEGMENT, s),
                a.on(u.a.FRAG_PARSING_DATA, s),
                a.on(u.a.FRAG_PARSED, s),
                a.on(u.a.ERROR, s),
                a.on(u.a.FRAG_PARSING_METADATA, s),
                a.on(u.a.FRAG_PARSING_USERDATA, s),
                a.on(u.a.INIT_PTS_FOUND, s);
                var f = {
                    mp4: v.isTypeSupported("video/mp4"),
                    mpeg: v.isTypeSupported("audio/mpeg"),
                    mp3: v.isTypeSupported('audio/mp4; codecs="mp3"')
                }
                  , p = navigator.vendor;
                if (n.enableWorker && "undefined" != typeof Worker) {
                    c.b.log("demuxing in webworker");
                    var y = void 0;
                    try {
                        y = this.w = l()(49),
                        this.onwmsg = this.onWorkerMessage.bind(this),
                        y.addEventListener("message", this.onwmsg),
                        y.onerror = function(t) {
                            e.trigger(u.a.ERROR, {
                                type: h.b.OTHER_ERROR,
                                details: h.a.INTERNAL_EXCEPTION,
                                fatal: !0,
                                event: "demuxerWorker",
                                err: {
                                    message: t.message + " (" + t.filename + ":" + t.lineno + ")"
                                }
                            })
                        }
                        ,
                        y.postMessage({
                            cmd: "init",
                            typeSupported: f,
                            vendor: p,
                            id: r,
                            config: JSON.stringify(n)
                        })
                    } catch (t) {
                        c.b.error("error while initializing DemuxerWorker, fallback on DemuxerInline"),
                        y && g.URL.revokeObjectURL(y.objectURL),
                        this.demuxer = new d.a(a,f,n,p),
                        this.w = void 0
                    }
                } else
                    this.demuxer = new d.a(a,f,n,p)
            }
            return t.prototype.destroy = function() {
                var t = this.w;
                if (t)
                    t.removeEventListener("message", this.onwmsg),
                    t.terminate(),
                    this.w = null;
                else {
                    var e = this.demuxer;
                    e && (e.destroy(),
                    this.demuxer = null)
                }
                var r = this.observer;
                r && (r.removeAllListeners(),
                this.observer = null)
            }
            ,
            t.prototype.push = function(t, e, r, i, n, o, s, l) {
                var u = this.w
                  , d = Object(a.a)(n.startDTS) ? n.startDTS : n.start
                  , h = n.decryptdata
                  , f = this.frag
                  , p = !(f && n.cc === f.cc)
                  , g = !(f && n.level === f.level)
                  , v = f && n.sn === f.sn + 1
                  , y = !g && v;
                if (p && c.b.log(this.id + ":discontinuity detected"),
                g && c.b.log(this.id + ":switch detected"),
                this.frag = n,
                u)
                    u.postMessage({
                        cmd: "demux",
                        data: t,
                        decryptdata: h,
                        initSegment: e,
                        audioCodec: r,
                        videoCodec: i,
                        timeOffset: d,
                        discontinuity: p,
                        trackSwitch: g,
                        contiguous: y,
                        duration: o,
                        accurateTimeOffset: s,
                        defaultInitPTS: l
                    }, t instanceof ArrayBuffer ? [t] : []);
                else {
                    var m = this.demuxer;
                    m && m.push(t, h, e, r, i, d, p, g, y, o, s, l)
                }
            }
            ,
            t.prototype.onWorkerMessage = function(t) {
                var e = t.data
                  , r = this.hls;
                switch (e.event) {
                case "init":
                    g.URL.revokeObjectURL(this.w.objectURL);
                    break;
                case u.a.FRAG_PARSING_DATA:
                    e.data.data1 = new Uint8Array(e.data1),
                    e.data2 && (e.data.data2 = new Uint8Array(e.data2));
                default:
                    e.data = e.data || {},
                    e.data.frag = this.frag,
                    e.data.id = this.id,
                    r.trigger(e.event, e.data)
                }
            }
            ,
            t
        }();
        e.a = y
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(1)
          , n = r(2)
          , o = r(14)
          , s = r(40)
          , l = r(18)
          , u = r(41)
          , d = r(44)
          , c = r(45)
          , h = r(48)
          , f = r(5)
          , p = Object(f.a)()
          , g = p.performance
          , v = function() {
            function t(e, r, a, n) {
                i(this, t),
                this.observer = e,
                this.typeSupported = r,
                this.config = a,
                this.vendor = n
            }
            return t.prototype.destroy = function() {
                var t = this.demuxer;
                t && t.destroy()
            }
            ,
            t.prototype.push = function(t, e, r, i, n, s, l, u, d, c, h, f) {
                if (t.byteLength > 0 && null != e && null != e.key && "AES-128" === e.method) {
                    var p = this.decrypter;
                    null == p && (p = this.decrypter = new o.a(this.observer,this.config));
                    var v = this
                      , y = void 0;
                    try {
                        y = g.now()
                    } catch (t) {
                        y = Date.now()
                    }
                    p.decrypt(t, e.key.buffer, e.iv.buffer, function(t) {
                        var o = void 0;
                        try {
                            o = g.now()
                        } catch (t) {
                            o = Date.now()
                        }
                        v.observer.trigger(a.a.FRAG_DECRYPTED, {
                            stats: {
                                tstart: y,
                                tdecrypt: o
                            }
                        }),
                        v.pushDecrypted(new Uint8Array(t), e, new Uint8Array(r), i, n, s, l, u, d, c, h, f)
                    })
                } else
                    this.pushDecrypted(new Uint8Array(t), e, new Uint8Array(r), i, n, s, l, u, d, c, h, f)
            }
            ,
            t.prototype.pushDecrypted = function(t, e, r, i, o, f, p, g, v, y, m, b) {
                var E = this.demuxer;
                if (!E || (p || g) && !this.probe(t)) {
                    for (var T = this.observer, S = this.typeSupported, A = this.config, R = [{
                        demux: u.a,
                        remux: c.a
                    }, {
                        demux: l.a,
                        remux: h.a
                    }, {
                        demux: s.a,
                        remux: c.a
                    }, {
                        demux: d.a,
                        remux: c.a
                    }], _ = 0, w = R.length; _ < w; _++) {
                        var L = R[_]
                          , D = L.demux.probe;
                        if (D(t)) {
                            var I = this.remuxer = new L.remux(T,A,S,this.vendor);
                            E = new L.demux(T,I,A,S),
                            this.probe = D;
                            break
                        }
                    }
                    if (!E)
                        return void T.trigger(a.a.ERROR, {
                            type: n.b.MEDIA_ERROR,
                            details: n.a.FRAG_PARSING_ERROR,
                            fatal: !0,
                            reason: "no demux matching with content found"
                        });
                    this.demuxer = E
                }
                var k = this.remuxer;
                (p || g) && (E.resetInitSegment(r, i, o, y),
                k.resetInitSegment()),
                p && (E.resetTimeStamp(b),
                k.resetTimeStamp(b)),
                "function" == typeof E.setDecryptData && E.setDecryptData(e),
                E.append(t, f, v, m)
            }
            ,
            t
        }();
        e.a = v
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e, r, i) {
            var a = void 0
              , n = void 0
              , o = void 0
              , s = void 0
              , l = void 0
              , u = navigator.userAgent.toLowerCase()
              , d = i
              , c = [96e3, 88200, 64e3, 48e3, 44100, 32e3, 24e3, 22050, 16e3, 12e3, 11025, 8e3, 7350];
            return a = 1 + ((192 & e[r + 2]) >>> 6),
            (n = (60 & e[r + 2]) >>> 2) > c.length - 1 ? void t.trigger(g.a.ERROR, {
                type: p.b.MEDIA_ERROR,
                details: p.a.FRAG_PARSING_ERROR,
                fatal: !0,
                reason: "invalid ADTS sampling index:" + n
            }) : (s = (1 & e[r + 2]) << 2,
            s |= (192 & e[r + 3]) >>> 6,
            f.b.log("manifest codec:" + i + ",ADTS data:type:" + a + ",sampleingIndex:" + n + "[" + c[n] + "Hz],channelConfig:" + s),
            /firefox/i.test(u) ? n >= 6 ? (a = 5,
            l = new Array(4),
            o = n - 3) : (a = 2,
            l = new Array(2),
            o = n) : -1 !== u.indexOf("android") ? (a = 2,
            l = new Array(2),
            o = n) : (a = 5,
            l = new Array(4),
            i && (-1 !== i.indexOf("mp4a.40.29") || -1 !== i.indexOf("mp4a.40.5")) || !i && n >= 6 ? o = n - 3 : ((i && -1 !== i.indexOf("mp4a.40.2") && (n >= 6 && 1 === s || /vivaldi/i.test(u)) || !i && 1 === s) && (a = 2,
            l = new Array(2)),
            o = n)),
            l[0] = a << 3,
            l[0] |= (14 & n) >> 1,
            l[1] |= (1 & n) << 7,
            l[1] |= s << 3,
            5 === a && (l[1] |= (14 & o) >> 1,
            l[2] = (1 & o) << 7,
            l[2] |= 8,
            l[3] = 0),
            {
                config: l,
                samplerate: c[n],
                channelCount: s,
                codec: "mp4a.40." + a,
                manifestCodec: d
            })
        }
        function a(t, e) {
            return 255 === t[e] && 240 == (246 & t[e + 1])
        }
        function n(t, e) {
            return 1 & t[e + 1] ? 7 : 9
        }
        function o(t, e) {
            return (3 & t[e + 3]) << 11 | t[e + 4] << 3 | (224 & t[e + 5]) >>> 5
        }
        function s(t, e) {
            return !!(e + 1 < t.length && a(t, e))
        }
        function l(t, e) {
            if (e + 1 < t.length && a(t, e)) {
                var r = n(t, e)
                  , i = r;
                e + 5 < t.length && (i = o(t, e));
                var s = e + i;
                if (s === t.length || s + 1 < t.length && a(t, s))
                    return !0
            }
            return !1
        }
        function u(t, e, r, a, n) {
            if (!t.samplerate) {
                var o = i(e, r, a, n);
                t.config = o.config,
                t.samplerate = o.samplerate,
                t.channelCount = o.channelCount,
                t.codec = o.codec,
                t.manifestCodec = o.manifestCodec,
                f.b.log("parsed codec:" + t.codec + ",rate:" + o.samplerate + ",nb channel:" + o.channelCount)
            }
        }
        function d(t) {
            return 9216e4 / t
        }
        function c(t, e, r, i, a) {
            var s = void 0
              , l = void 0
              , u = void 0
              , d = t.length;
            if (s = n(t, e),
            l = o(t, e),
            (l -= s) > 0 && e + s + l <= d)
                return u = r + i * a,
                {
                    headerLength: s,
                    frameLength: l,
                    stamp: u
                }
        }
        function h(t, e, r, i, a) {
            var n = d(t.samplerate)
              , o = c(e, r, i, a, n);
            if (o) {
                var s = o.stamp
                  , l = o.headerLength
                  , u = o.frameLength
                  , h = {
                    unit: e.subarray(r + l, r + l + u),
                    pts: s,
                    dts: s
                };
                return t.samples.push(h),
                t.len += u,
                {
                    sample: h,
                    length: u + l
                }
            }
        }
        e.d = s,
        e.e = l,
        e.c = u,
        e.b = d,
        e.a = h;
        var f = r(0)
          , p = r(2)
          , g = r(1);
        r(5)
    }
    , function(t, e, r) {
        "use strict";
        var i = {
            BitratesMap: [32, 64, 96, 128, 160, 192, 224, 256, 288, 320, 352, 384, 416, 448, 32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320, 384, 32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320, 32, 48, 56, 64, 80, 96, 112, 128, 144, 160, 176, 192, 224, 256, 8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 128, 144, 160],
            SamplingRateMap: [44100, 48e3, 32e3, 22050, 24e3, 16e3, 11025, 12e3, 8e3],
            SamplesCoefficients: [[0, 72, 144, 12], [0, 0, 0, 0], [0, 72, 144, 12], [0, 144, 144, 12]],
            BytesInSlot: [0, 1, 1, 4],
            appendFrame: function(t, e, r, i, a) {
                if (!(r + 24 > e.length)) {
                    var n = this.parseHeader(e, r);
                    if (n && r + n.frameLength <= e.length) {
                        var o = 9e4 * n.samplesPerFrame / n.sampleRate
                          , s = i + a * o
                          , l = {
                            unit: e.subarray(r, r + n.frameLength),
                            pts: s,
                            dts: s
                        };
                        return t.config = [],
                        t.channelCount = n.channelCount,
                        t.samplerate = n.sampleRate,
                        t.samples.push(l),
                        t.len += n.frameLength,
                        {
                            sample: l,
                            length: n.frameLength
                        }
                    }
                }
            },
            parseHeader: function(t, e) {
                var r = t[e + 1] >> 3 & 3
                  , a = t[e + 1] >> 1 & 3
                  , n = t[e + 2] >> 4 & 15
                  , o = t[e + 2] >> 2 & 3
                  , s = t[e + 2] >> 1 & 1;
                if (1 !== r && 0 !== n && 15 !== n && 3 !== o) {
                    var l = 3 === r ? 3 - a : 3 === a ? 3 : 4
                      , u = 1e3 * i.BitratesMap[14 * l + n - 1]
                      , d = 3 === r ? 0 : 2 === r ? 1 : 2
                      , c = i.SamplingRateMap[3 * d + o]
                      , h = t[e + 3] >> 6 == 3 ? 1 : 2
                      , f = i.SamplesCoefficients[r][a]
                      , p = i.BytesInSlot[a]
                      , g = 8 * f * p;
                    return {
                        sampleRate: c,
                        channelCount: h,
                        frameLength: parseInt(f * u / c + s, 10) * p,
                        samplesPerFrame: g
                    }
                }
            },
            isHeaderPattern: function(t, e) {
                return 255 === t[e] && 224 == (224 & t[e + 1]) && 0 != (6 & t[e + 1])
            },
            isHeader: function(t, e) {
                return !!(e + 1 < t.length && this.isHeaderPattern(t, e))
            },
            probe: function(t, e) {
                if (e + 1 < t.length && this.isHeaderPattern(t, e)) {
                    var r = this.parseHeader(t, e)
                      , i = 4;
                    r && r.frameLength && (i = r.frameLength);
                    var a = e + i;
                    if (a === t.length || a + 1 < t.length && this.isHeaderPattern(t, a))
                        return !0
                }
                return !1
            }
        };
        e.a = i
    }
    , function(t, e, r) {
        "use strict";
        var i = {
            toString: function(t) {
                for (var e = "", r = t.length, i = 0; i < r; i++)
                    e += "[" + t.start(i).toFixed(3) + "," + t.end(i).toFixed(3) + "]";
                return e
            }
        };
        e.a = i
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            for (var r = null, i = 0; i < t.length; i += 1) {
                var a = t[i];
                if (a && a.cc === e) {
                    r = a;
                    break
                }
            }
            return r
        }
        function a(t, e) {
            return h.a.search(t, function(t) {
                return t.cc < e ? 1 : t.cc > e ? -1 : 0
            })
        }
        function n(t, e, r) {
            var i = !1;
            return e && e.details && r && (r.endCC > r.startCC || t && t.cc < r.startCC) && (i = !0),
            i
        }
        function o(t, e) {
            var r = t.fragments
              , a = e.fragments;
            if (!a.length || !r.length)
                return void f.b.log("No fragments to align");
            var n = i(r, a[0].cc);
            return !n || n && !n.startPTS ? void f.b.log("No frag in previous level to align on") : n
        }
        function s(t, e) {
            e.fragments.forEach(function(e) {
                if (e) {
                    var r = e.start + t;
                    e.start = e.startPTS = r,
                    e.endPTS = r + e.duration
                }
            }),
            e.PTSKnown = !0
        }
        function l(t, e, r) {
            u(t, r, e),
            !r.PTSKnown && e && d(r, e.details)
        }
        function u(t, e, r) {
            if (n(t, r, e)) {
                var i = o(r.details, e);
                i && (f.b.log("Adjusting PTS using last level due to CC increase within current level"),
                s(i.start, e))
            }
        }
        function d(t, e) {
            if (e && e.fragments.length) {
                if (!t.hasProgramDateTime || !e.hasProgramDateTime)
                    return;
                var r = e.fragments[0].programDateTime
                  , i = t.fragments[0].programDateTime
                  , a = (i - r) / 1e3 + e.fragments[0].start;
                Object(c.a)(a) && (f.b.log("adjusting PTS using programDateTime delta, sliding:" + a.toFixed(3)),
                s(a, t))
            }
        }
        e.b = a,
        e.a = l;
        var c = r(3)
          , h = r(7)
          , f = r(0)
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            var r = null;
            try {
                r = new window.Event("addtrack")
            } catch (t) {
                r = document.createEvent("Event"),
                r.initEvent("addtrack", !1, !1)
            }
            r.track = t,
            e.dispatchEvent(r)
        }
        function a(t) {
            if (t && t.cues)
                for (; t.cues.length > 0; )
                    t.removeCue(t.cues[0])
        }
        e.b = i,
        e.a = a
    }
    , function(t, e, r) {
        "use strict";
        function i() {
            this.window = window,
            this.state = "INITIAL",
            this.buffer = "",
            this.decoder = new d,
            this.regionList = []
        }
        function a(t) {
            function e(t, e, r, i) {
                return 3600 * (0 | t) + 60 * (0 | e) + (0 | r) + (0 | i) / 1e3
            }
            var r = t.match(/^(\d+):(\d{2})(:\d{2})?\.(\d{3})/);
            return r ? r[3] ? e(r[1], r[2], r[3].replace(":", ""), r[4]) : r[1] > 59 ? e(r[1], r[2], 0, r[4]) : e(0, r[1], r[2], r[4]) : null
        }
        function n() {
            this.values = Object.create(null)
        }
        function o(t, e, r, i) {
            var a = i ? t.split(i) : [t];
            for (var n in a)
                if ("string" == typeof a[n]) {
                    var o = a[n].split(r);
                    if (2 === o.length) {
                        var s = o[0]
                          , l = o[1];
                        e(s, l)
                    }
                }
        }
        function s(t, e, r) {
            function i() {
                var e = a(t);
                if (null === e)
                    throw new Error("Malformed timestamp: " + l);
                return t = t.replace(/^[^\sa-zA-Z-]+/, ""),
                e
            }
            function s() {
                t = t.replace(/^\s+/, "")
            }
            var l = t;
            if (s(),
            e.startTime = i(),
            s(),
            "--\x3e" !== t.substr(0, 3))
                throw new Error("Malformed time stamp (time stamps must be separated by '--\x3e'): " + l);
            t = t.substr(3),
            s(),
            e.endTime = i(),
            s(),
            function(t, e) {
                var i = new n;
                o(t, function(t, e) {
                    switch (t) {
                    case "region":
                        for (var a = r.length - 1; a >= 0; a--)
                            if (r[a].id === e) {
                                i.set(t, r[a].region);
                                break
                            }
                        break;
                    case "vertical":
                        i.alt(t, e, ["rl", "lr"]);
                        break;
                    case "line":
                        var n = e.split(",")
                          , o = n[0];
                        i.integer(t, o),
                        i.percent(t, o) && i.set("snapToLines", !1),
                        i.alt(t, o, ["auto"]),
                        2 === n.length && i.alt("lineAlign", n[1], ["start", h, "end"]);
                        break;
                    case "position":
                        n = e.split(","),
                        i.percent(t, n[0]),
                        2 === n.length && i.alt("positionAlign", n[1], ["start", h, "end", "line-left", "line-right", "auto"]);
                        break;
                    case "size":
                        i.percent(t, e);
                        break;
                    case "align":
                        i.alt(t, e, ["start", h, "end", "left", "right"])
                    }
                }, /:/, /\s/),
                e.region = i.get("region", null),
                e.vertical = i.get("vertical", "");
                var a = i.get("line", "auto");
                "auto" === a && -1 === c.line && (a = -1),
                e.line = a,
                e.lineAlign = i.get("lineAlign", "start"),
                e.snapToLines = i.get("snapToLines", !0),
                e.size = i.get("size", 100),
                e.align = i.get("align", h);
                var s = i.get("position", "auto");
                "auto" === s && 50 === c.position && (s = "start" === e.align || "left" === e.align ? 0 : "end" === e.align || "right" === e.align ? 100 : 50),
                e.position = s
            }(t, e)
        }
        function l(t) {
            return t.replace(/<br(?: \/)?>/gi, "\n")
        }
        r.d(e, "b", function() {
            return l
        });
        var u = r(66)
          , d = function() {
            return {
                decode: function(t) {
                    if (!t)
                        return "";
                    if ("string" != typeof t)
                        throw new Error("Error - expected string data.");
                    return decodeURIComponent(encodeURIComponent(t))
                }
            }
        };
        n.prototype = {
            set: function(t, e) {
                this.get(t) || "" === e || (this.values[t] = e)
            },
            get: function(t, e, r) {
                return r ? this.has(t) ? this.values[t] : e[r] : this.has(t) ? this.values[t] : e
            },
            has: function(t) {
                return t in this.values
            },
            alt: function(t, e, r) {
                for (var i = 0; i < r.length; ++i)
                    if (e === r[i]) {
                        this.set(t, e);
                        break
                    }
            },
            integer: function(t, e) {
                /^-?\d+$/.test(e) && this.set(t, parseInt(e, 10))
            },
            percent: function(t, e) {
                return !!(e.match(/^([\d]{1,3})(\.[\d]*)?%$/) && (e = parseFloat(e)) >= 0 && e <= 100) && (this.set(t, e),
                !0)
            }
        };
        var c = new u.a(0,0,0)
          , h = "middle" === c.align ? "middle" : "center";
        i.prototype = {
            parse: function(t) {
                function e() {
                    var t = r.buffer
                      , e = 0;
                    for (t = l(t); e < t.length && "\r" !== t[e] && "\n" !== t[e]; )
                        ++e;
                    var i = t.substr(0, e);
                    return "\r" === t[e] && ++e,
                    "\n" === t[e] && ++e,
                    r.buffer = t.substr(e),
                    i
                }
                var r = this;
                t && (r.buffer += r.decoder.decode(t, {
                    stream: !0
                }));
                try {
                    var i = void 0;
                    if ("INITIAL" === r.state) {
                        if (!/\r\n|\n/.test(r.buffer))
                            return this;
                        i = e();
                        var a = i.match(/^(ï»¿)?WEBVTT([ \t].*)?$/);
                        if (!a || !a[0])
                            throw new Error("Malformed WebVTT signature.");
                        r.state = "HEADER"
                    }
                    for (var n = !1; r.buffer; ) {
                        if (!/\r\n|\n/.test(r.buffer))
                            return this;
                        switch (n ? n = !1 : i = e(),
                        r.state) {
                        case "HEADER":
                            /:/.test(i) ? function(t) {
                                o(t, function(t, e) {}, /:/)
                            }(i) : i || (r.state = "ID");
                            continue;
                        case "NOTE":
                            i || (r.state = "ID");
                            continue;
                        case "ID":
                            if (/^NOTE($|[ \t])/.test(i)) {
                                r.state = "NOTE";
                                break
                            }
                            if (!i)
                                continue;
                            if (r.cue = new u.a(0,0,""),
                            r.state = "CUE",
                            -1 === i.indexOf("--\x3e")) {
                                r.cue.id = i;
                                continue
                            }
                        case "CUE":
                            try {
                                s(i, r.cue, r.regionList)
                            } catch (t) {
                                r.cue = null,
                                r.state = "BADCUE";
                                continue
                            }
                            r.state = "CUETEXT";
                            continue;
                        case "CUETEXT":
                            var d = -1 !== i.indexOf("--\x3e");
                            if (!i || d && (n = !0)) {
                                r.oncue && r.oncue(r.cue),
                                r.cue = null,
                                r.state = "ID";
                                continue
                            }
                            r.cue.text && (r.cue.text += "\n"),
                            r.cue.text += i;
                            continue;
                        case "BADCUE":
                            i || (r.state = "ID");
                            continue
                        }
                    }
                } catch (t) {
                    "CUETEXT" === r.state && r.cue && r.oncue && r.oncue(r.cue),
                    r.cue = null,
                    r.state = "INITIAL" === r.state ? "BADWEBVTT" : "BADCUE"
                }
                return this
            },
            flush: function() {
                var t = this;
                try {
                    if (t.buffer += t.decoder.decode(),
                    (t.cue || "HEADER" === t.state) && (t.buffer += "\n\n",
                    t.parse()),
                    "INITIAL" === t.state)
                        throw new Error("Malformed WebVTT signature.")
                } catch (t) {
                    throw t
                }
                return t.onflush && t.onflush(),
                this
            }
        },
        e.a = i
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        Object.defineProperty(e, "__esModule", {
            value: !0
        });
        var a = r(6)
          , n = r.n(a)
          , o = r(2)
          , s = r(17)
          , l = r(33)
          , u = r(34)
          , d = r(12)
          , c = r(35)
          , h = r(52)
          , f = r(53)
          , p = r(54)
          , g = r(0)
          , v = r(55)
          , y = r(1)
          , m = r(13)
          , b = r.n(m)
          , E = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }();
        r(75);
        var T = function() {
            function t() {
                var e = this
                  , r = arguments.length > 0 && void 0 !== arguments[0] ? arguments[0] : {};
                i(this, t);
                var a = t.DefaultConfig;
                if ((r.liveSyncDurationCount || r.liveMaxLatencyDurationCount) && (r.liveSyncDuration || r.liveMaxLatencyDuration))
                    throw new Error("Illegal hls.js config: don't mix up liveSyncDurationCount/liveMaxLatencyDurationCount and liveSyncDuration/liveMaxLatencyDuration");
                for (var n in a)
                    n in r || (r[n] = a[n]);
                if (void 0 !== r.liveMaxLatencyDurationCount && r.liveMaxLatencyDurationCount <= r.liveSyncDurationCount)
                    throw new Error('Illegal hls.js config: "liveMaxLatencyDurationCount" must be gt "liveSyncDurationCount"');
                if (void 0 !== r.liveMaxLatencyDuration && (r.liveMaxLatencyDuration <= r.liveSyncDuration || void 0 === r.liveSyncDuration))
                    throw new Error('Illegal hls.js config: "liveMaxLatencyDuration" must be gt "liveSyncDuration"');
                Object(g.a)(r.debug),
                this.config = r,
                this._autoLevelCapping = -1;
                var o = this.observer = new b.a;
                o.trigger = function(t) {
                    for (var e = arguments.length, r = Array(e > 1 ? e - 1 : 0), i = 1; i < e; i++)
                        r[i - 1] = arguments[i];
                    o.emit.apply(o, [t, t].concat(r))
                }
                ,
                o.off = function(t) {
                    for (var e = arguments.length, r = Array(e > 1 ? e - 1 : 0), i = 1; i < e; i++)
                        r[i - 1] = arguments[i];
                    o.removeListener.apply(o, [t].concat(r))
                }
                ,
                this.on = o.on.bind(o),
                this.off = o.off.bind(o),
                this.once = o.once.bind(o),
                this.trigger = o.trigger.bind(o);
                var p = this.abrController = new r.abrController(this)
                  , v = new r.bufferController(this)
                  , y = new r.capLevelController(this)
                  , m = new r.fpsController(this)
                  , E = new s.a(this)
                  , T = new l.a(this)
                  , S = new u.a(this)
                  , A = new f.a(this)
                  , R = this.levelController = new h.a(this)
                  , _ = new d.b(this)
                  , w = this.streamController = new c.a(this,_)
                  , L = [R, w]
                  , D = r.audioStreamController;
                D && L.push(new D(this,_)),
                this.networkControllers = L;
                var I = [E, T, S, p, v, y, m, A, _];
                if (D = r.audioTrackController) {
                    var k = new D(this);
                    this.audioTrackController = k,
                    I.push(k)
                }
                if (D = r.subtitleTrackController) {
                    var O = new D(this);
                    this.subtitleTrackController = O,
                    I.push(O)
                }
                if (D = r.emeController) {
                    var C = new D(this);
                    this.emeController = C,
                    I.push(C)
                }
                [r.subtitleStreamController, r.timelineController].forEach(function(t) {
                    t && I.push(new t(e))
                }),
                this.coreComponents = I
            }
            return t.isSupported = function() {
                return Object(p.a)()
            }
            ,
            E(t, null, [{
                key: "version",
                get: function() {
                    return "0.11.0"
                }
            }, {
                key: "Events",
                get: function() {
                    return y.a
                }
            }, {
                key: "ErrorTypes",
                get: function() {
                    return o.b
                }
            }, {
                key: "ErrorDetails",
                get: function() {
                    return o.a
                }
            }, {
                key: "DefaultConfig",
                get: function() {
                    return t.defaultConfig ? t.defaultConfig : v.a
                },
                set: function(e) {
                    t.defaultConfig = e
                }
            }]),
            t.prototype.destroy = function() {
                g.b.log("destroy"),
                this.trigger(y.a.DESTROYING),
                this.detachMedia(),
                this.coreComponents.concat(this.networkControllers).forEach(function(t) {
                    t.destroy()
                }),
                this.url = null,
                this.observer.removeAllListeners(),
                this._autoLevelCapping = -1
            }
            ,
            t.prototype.attachMedia = function(t) {
                g.b.log("attachMedia"),
                this.media = t,
                this.trigger(y.a.MEDIA_ATTACHING, {
                    media: t
                })
            }
            ,
            t.prototype.detachMedia = function() {
                g.b.log("detachMedia"),
                this.trigger(y.a.MEDIA_DETACHING),
                this.media = null
            }
            ,
            t.prototype.loadSource = function(t) {
                t = n.a.buildAbsoluteURL(window.location.href, t, {
                    alwaysNormalize: !0
                }),
                g.b.log("loadSource:" + t),
                this.url = t,
                this.trigger(y.a.MANIFEST_LOADING, {
                    url: t
                })
            }
            ,
            t.prototype.startLoad = function() {
                var t = arguments.length > 0 && void 0 !== arguments[0] ? arguments[0] : -1;
                g.b.log("startLoad(" + t + ")"),
                this.networkControllers.forEach(function(e) {
                    e.startLoad(t)
                })
            }
            ,
            t.prototype.stopLoad = function() {
                g.b.log("stopLoad"),
                this.networkControllers.forEach(function(t) {
                    t.stopLoad()
                })
            }
            ,
            t.prototype.swapAudioCodec = function() {
                g.b.log("swapAudioCodec"),
                this.streamController.swapAudioCodec()
            }
            ,
            t.prototype.recoverMediaError = function() {
                g.b.log("recoverMediaError");
                var t = this.media;
                this.detachMedia(),
                this.attachMedia(t)
            }
            ,
            E(t, [{
                key: "levels",
                get: function() {
                    return this.levelController.levels
                }
            }, {
                key: "currentLevel",
                get: function() {
                    return this.streamController.currentLevel
                },
                set: function(t) {
                    g.b.log("set currentLevel:" + t),
                    this.loadLevel = t,
                    this.streamController.immediateLevelSwitch()
                }
            }, {
                key: "nextLevel",
                get: function() {
                    return this.streamController.nextLevel
                },
                set: function(t) {
                    g.b.log("set nextLevel:" + t),
                    this.levelController.manualLevel = t,
                    this.streamController.nextLevelSwitch()
                }
            }, {
                key: "loadLevel",
                get: function() {
                    return this.levelController.level
                },
                set: function(t) {
                    g.b.log("set loadLevel:" + t),
                    this.levelController.manualLevel = t
                }
            }, {
                key: "nextLoadLevel",
                get: function() {
                    return this.levelController.nextLoadLevel
                },
                set: function(t) {
                    this.levelController.nextLoadLevel = t
                }
            }, {
                key: "firstLevel",
                get: function() {
                    return Math.max(this.levelController.firstLevel, this.minAutoLevel)
                },
                set: function(t) {
                    g.b.log("set firstLevel:" + t),
                    this.levelController.firstLevel = t
                }
            }, {
                key: "startLevel",
                get: function() {
                    return this.levelController.startLevel
                },
                set: function(t) {
                    g.b.log("set startLevel:" + t);
                    var e = this;
                    -1 !== t && (t = Math.max(t, e.minAutoLevel)),
                    e.levelController.startLevel = t
                }
            }, {
                key: "autoLevelCapping",
                get: function() {
                    return this._autoLevelCapping
                },
                set: function(t) {
                    g.b.log("set autoLevelCapping:" + t),
                    this._autoLevelCapping = t
                }
            }, {
                key: "autoLevelEnabled",
                get: function() {
                    return -1 === this.levelController.manualLevel
                }
            }, {
                key: "manualLevel",
                get: function() {
                    return this.levelController.manualLevel
                }
            }, {
                key: "minAutoLevel",
                get: function() {
                    for (var t = this, e = t.levels, r = t.config.minAutoBitrate, i = e ? e.length : 0, a = 0; a < i; a++) {
                        if ((e[a].realBitrate ? Math.max(e[a].realBitrate, e[a].bitrate) : e[a].bitrate) > r)
                            return a
                    }
                    return 0
                }
            }, {
                key: "maxAutoLevel",
                get: function() {
                    var t = this
                      , e = t.levels
                      , r = t.autoLevelCapping;
                    return -1 === r && e && e.length ? e.length - 1 : r
                }
            }, {
                key: "nextAutoLevel",
                get: function() {
                    var t = this;
                    return Math.min(Math.max(t.abrController.nextAutoLevel, t.minAutoLevel), t.maxAutoLevel)
                },
                set: function(t) {
                    var e = this;
                    e.abrController.nextAutoLevel = Math.max(e.minAutoLevel, t)
                }
            }, {
                key: "audioTracks",
                get: function() {
                    var t = this.audioTrackController;
                    return t ? t.audioTracks : []
                }
            }, {
                key: "audioTrack",
                get: function() {
                    var t = this.audioTrackController;
                    return t ? t.audioTrack : -1
                },
                set: function(t) {
                    var e = this.audioTrackController;
                    e && (e.audioTrack = t)
                }
            }, {
                key: "liveSyncPosition",
                get: function() {
                    return this.streamController.liveSyncPosition
                }
            }, {
                key: "subtitleTracks",
                get: function() {
                    var t = this.subtitleTrackController;
                    return t ? t.subtitleTracks : []
                }
            }, {
                key: "subtitleTrack",
                get: function() {
                    var t = this.subtitleTrackController;
                    return t ? t.subtitleTrack : -1
                },
                set: function(t) {
                    var e = this.subtitleTrackController;
                    e && (e.subtitleTrack = t)
                }
            }, {
                key: "subtitleDisplay",
                get: function() {
                    var t = this.subtitleTrackController;
                    return !!t && t.subtitleDisplay
                },
                set: function(t) {
                    var e = this.subtitleTrackController;
                    e && (e.subtitleDisplay = t)
                }
            }]),
            t
        }();
        e.default = T
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            for (var r = t[e], i = e - 1; i >= 0; i--) {
                var a = t[i];
                a.programDateTime = r.programDateTime - 1e3 * a.duration,
                r = a
            }
        }
        function n(t, e) {
            t.rawProgramDateTime ? t.programDateTime = Date.parse(t.rawProgramDateTime) : e && e.programDateTime && (t.programDateTime = e.endProgramDateTime),
            Object(o.a)(t.programDateTime) || (t.programDateTime = null,
            t.rawProgramDateTime = null)
        }
        var o = r(3)
          , s = r(6)
          , l = r.n(s)
          , u = r(11)
          , d = r(31)
          , c = r(19)
          , h = r(32)
          , f = r(0)
          , p = r(20)
          , g = /#EXT-X-STREAM-INF:([^\n\r]*)[\r\n]+([^\r\n]+)/g
          , v = /#EXT-X-MEDIA:(.*)/g
          , y = new RegExp([/#EXTINF:\s*(\d*(?:\.\d+)?)(?:,(.*)\s+)?/.source, /|(?!#)(\S+)/.source, /|#EXT-X-BYTERANGE:*(.+)/.source, /|#EXT-X-PROGRAM-DATE-TIME:(.+)/.source, /|#.*/.source].join(""),"g")
          , m = /(?:(?:#(EXTM3U))|(?:#EXT-X-(PLAYLIST-TYPE):(.+))|(?:#EXT-X-(MEDIA-SEQUENCE): *(\d+))|(?:#EXT-X-(TARGETDURATION): *(\d+))|(?:#EXT-X-(KEY):(.+))|(?:#EXT-X-(START):(.+))|(?:#EXT-X-(ENDLIST))|(?:#EXT-X-(DISCONTINUITY-SEQ)UENCE:(\d+))|(?:#EXT-X-(DIS)CONTINUITY))|(?:#EXT-X-(VERSION):(\d+))|(?:#EXT-X-(MAP):(.+))|(?:(#)([^:]*):(.*))|(?:(#)(.*))(?:.*)\r?\n?/
          , b = /\.(mp4|m4s|m4v|m4a)$/i
          , E = function() {
            function t() {
                i(this, t)
            }
            return t.findGroup = function(t, e) {
                if (!t)
                    return null;
                for (var r = null, i = 0; i < t.length; i++) {
                    var a = t[i];
                    a.id === e && (r = a)
                }
                return r
            }
            ,
            t.convertAVC1ToAVCOTI = function(t) {
                var e = void 0
                  , r = t.split(".");
                return r.length > 2 ? (e = r.shift() + ".",
                e += parseInt(r.shift()).toString(16),
                e += ("000" + parseInt(r.shift()).toString(16)).substr(-4)) : e = t,
                e
            }
            ,
            t.resolve = function(t, e) {
                return l.a.buildAbsoluteURL(e, t, {
                    alwaysNormalize: !0
                })
            }
            ,
            t.parseMasterPlaylist = function(e, r) {
                var i = []
                  , a = void 0;
                for (g.lastIndex = 0; null != (a = g.exec(e)); ) {
                    var n = {}
                      , o = n.attrs = new h.a(a[1]);
                    n.url = t.resolve(a[2], r);
                    var s = o.decimalResolution("RESOLUTION");
                    s && (n.width = s.width,
                    n.height = s.height),
                    n.bitrate = o.decimalInteger("AVERAGE-BANDWIDTH") || o.decimalInteger("BANDWIDTH"),
                    n.name = o.NAME,
                    function(t, e) {
                        ["video", "audio"].forEach(function(r) {
                            var i = t.filter(function(t) {
                                return Object(p.b)(t, r)
                            });
                            if (i.length) {
                                var a = i.filter(function(t) {
                                    return 0 === t.lastIndexOf("avc1", 0) || 0 === t.lastIndexOf("mp4a", 0)
                                });
                                e[r + "Codec"] = a.length > 0 ? a[0] : i[0],
                                t = t.filter(function(t) {
                                    return -1 === i.indexOf(t)
                                })
                            }
                        }),
                        e.unknownCodecs = t
                    }([].concat((o.CODECS || "").split(/[ ,]+/)), n),
                    n.videoCodec && -1 !== n.videoCodec.indexOf("avc1") && (n.videoCodec = t.convertAVC1ToAVCOTI(n.videoCodec)),
                    i.push(n)
                }
                return i
            }
            ,
            t.parseMasterPlaylistMedia = function(e, r, i) {
                var a = arguments.length > 3 && void 0 !== arguments[3] ? arguments[3] : []
                  , n = void 0
                  , o = []
                  , s = 0;
                for (v.lastIndex = 0; null !== (n = v.exec(e)); ) {
                    var l = {}
                      , u = new h.a(n[1]);
                    if (u.TYPE === i) {
                        if (l.groupId = u["GROUP-ID"],
                        l.name = u.NAME,
                        l.type = i,
                        l.default = "YES" === u.DEFAULT,
                        l.autoselect = "YES" === u.AUTOSELECT,
                        l.forced = "YES" === u.FORCED,
                        u.URI && (l.url = t.resolve(u.URI, r)),
                        l.lang = u.LANGUAGE,
                        l.name || (l.name = l.lang),
                        a.length) {
                            var d = t.findGroup(a, l.groupId);
                            l.audioCodec = d ? d.codec : a[0].codec
                        }
                        l.id = s++,
                        o.push(l)
                    }
                }
                return o
            }
            ,
            t.parseLevelPlaylist = function(t, e, r, i, s) {
                var l = 0
                  , p = 0
                  , g = new d.a(e)
                  , v = new c.a
                  , E = 0
                  , T = null
                  , S = new u.a
                  , A = void 0
                  , R = void 0
                  , _ = null;
                for (y.lastIndex = 0; null !== (A = y.exec(t)); ) {
                    var w = A[1];
                    if (w) {
                        S.duration = parseFloat(w);
                        var L = (" " + A[2]).slice(1);
                        S.title = L || null,
                        S.tagList.push(L ? ["INF", w, L] : ["INF", w])
                    } else if (A[3]) {
                        if (Object(o.a)(S.duration)) {
                            var D = l++;
                            S.type = i,
                            S.start = p,
                            S.levelkey = v,
                            S.sn = D,
                            S.level = r,
                            S.cc = E,
                            S.urlId = s,
                            S.baseurl = e,
                            S.relurl = (" " + A[3]).slice(1),
                            n(S, T),
                            g.fragments.push(S),
                            T = S,
                            p += S.duration,
                            S = new u.a
                        }
                    } else if (A[4]) {
                        if (S.rawByteRange = (" " + A[4]).slice(1),
                        T) {
                            var I = T.byteRangeEndOffset;
                            I && (S.lastByteRangeEndOffset = I)
                        }
                    } else if (A[5])
                        S.rawProgramDateTime = (" " + A[5]).slice(1),
                        S.tagList.push(["PROGRAM-DATE-TIME", S.rawProgramDateTime]),
                        null === _ && (_ = g.fragments.length);
                    else {
                        for (A = A[0].match(m),
                        R = 1; R < A.length && void 0 === A[R]; R++)
                            ;
                        var k = (" " + A[R + 1]).slice(1)
                          , O = (" " + A[R + 2]).slice(1);
                        switch (A[R]) {
                        case "#":
                            S.tagList.push(O ? [k, O] : [k]);
                            break;
                        case "PLAYLIST-TYPE":
                            g.type = k.toUpperCase();
                            break;
                        case "MEDIA-SEQUENCE":
                            l = g.startSN = parseInt(k);
                            break;
                        case "TARGETDURATION":
                            g.targetduration = parseFloat(k);
                            break;
                        case "VERSION":
                            g.version = parseInt(k);
                            break;
                        case "EXTM3U":
                            break;
                        case "ENDLIST":
                            g.live = !1;
                            break;
                        case "DIS":
                            E++,
                            S.tagList.push(["DIS"]);
                            break;
                        case "DISCONTINUITY-SEQ":
                            E = parseInt(k);
                            break;
                        case "KEY":
                            var C = k
                              , P = new h.a(C)
                              , x = P.enumeratedString("METHOD")
                              , F = P.URI
                              , M = P.hexadecimalInteger("IV");
                            x && (v = new c.a,
                            F && ["AES-128", "SAMPLE-AES", "SAMPLE-AES-CENC"].indexOf(x) >= 0 && (v.method = x,
                            v.baseuri = e,
                            v.reluri = F,
                            v.key = null,
                            v.iv = M));
                            break;
                        case "START":
                            var N = k
                              , U = new h.a(N)
                              , B = U.decimalFloatingPoint("TIME-OFFSET");
                            Object(o.a)(B) && (g.startTimeOffset = B);
                            break;
                        case "MAP":
                            var G = new h.a(k);
                            S.relurl = G.URI,
                            S.rawByteRange = G.BYTERANGE,
                            S.baseurl = e,
                            S.level = r,
                            S.type = i,
                            S.sn = "initSegment",
                            g.initSegment = S,
                            S = new u.a,
                            S.rawProgramDateTime = g.initSegment.rawProgramDateTime;
                            break;
                        default:
                            f.b.warn("line parsed but not handled: " + A)
                        }
                    }
                }
                return S = T,
                S && !S.relurl && (g.fragments.pop(),
                p -= S.duration),
                g.totalduration = p,
                g.averagetargetduration = p / g.fragments.length,
                g.endSN = l - 1,
                g.startCC = g.fragments[0] ? g.fragments[0].cc : 0,
                g.endCC = E,
                !g.initSegment && g.fragments.length && g.fragments.every(function(t) {
                    return b.test(t.relurl)
                }) && (f.b.warn("MP4 fragments found but no init segment (probably no MAP, incomplete M3U8), trying to fetch SIDX"),
                S = new u.a,
                S.relurl = g.fragments[0].relurl,
                S.baseurl = e,
                S.level = r,
                S.type = i,
                S.sn = "initSegment",
                g.initSegment = S,
                g.needSidxRanges = !0),
                _ && a(g.fragments, _),
                g
            }
            ,
            t
        }();
        e.a = E
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(3)
          , n = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , o = function() {
            function t(e) {
                i(this, t),
                this.endCC = 0,
                this.endSN = 0,
                this.fragments = [],
                this.initSegment = null,
                this.live = !0,
                this.needSidxRanges = !1,
                this.startCC = 0,
                this.startSN = 0,
                this.startTimeOffset = null,
                this.targetduration = 0,
                this.totalduration = 0,
                this.type = null,
                this.url = e,
                this.version = null
            }
            return n(t, [{
                key: "hasProgramDateTime",
                get: function() {
                    return !(!this.fragments[0] || !Object(a.a)(this.fragments[0].programDateTime))
                }
            }]),
            t
        }();
        e.a = o
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = /^(\d+)x(\d+)$/
          , n = /\s*(.+?)\s*=((?:\".*?\")|.*?)(?:,|$)/g
          , o = function() {
            function t(e) {
                i(this, t),
                "string" == typeof e && (e = t.parseAttrList(e));
                for (var r in e)
                    e.hasOwnProperty(r) && (this[r] = e[r])
            }
            return t.prototype.decimalInteger = function(t) {
                var e = parseInt(this[t], 10);
                return e > Number.MAX_SAFE_INTEGER ? 1 / 0 : e
            }
            ,
            t.prototype.hexadecimalInteger = function(t) {
                if (this[t]) {
                    var e = (this[t] || "0x").slice(2);
                    e = (1 & e.length ? "0" : "") + e;
                    for (var r = new Uint8Array(e.length / 2), i = 0; i < e.length / 2; i++)
                        r[i] = parseInt(e.slice(2 * i, 2 * i + 2), 16);
                    return r
                }
                return null
            }
            ,
            t.prototype.hexadecimalIntegerAsNumber = function(t) {
                var e = parseInt(this[t], 16);
                return e > Number.MAX_SAFE_INTEGER ? 1 / 0 : e
            }
            ,
            t.prototype.decimalFloatingPoint = function(t) {
                return parseFloat(this[t])
            }
            ,
            t.prototype.enumeratedString = function(t) {
                return this[t]
            }
            ,
            t.prototype.decimalResolution = function(t) {
                var e = a.exec(this[t]);
                if (null !== e)
                    return {
                        width: parseInt(e[1], 10),
                        height: parseInt(e[2], 10)
                    }
            }
            ,
            t.parseAttrList = function(t) {
                var e = void 0
                  , r = {};
                for (n.lastIndex = 0; null !== (e = n.exec(t)); ) {
                    var i = e[2];
                    0 === i.indexOf('"') && i.lastIndexOf('"') === i.length - 1 && (i = i.slice(1, -1)),
                    r[e[1]] = i
                }
                return r
            }
            ,
            t
        }();
        e.a = o
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(3)
          , s = r(1)
          , l = r(4)
          , u = r(2)
          , d = r(0)
          , c = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, s.a.FRAG_LOADING));
                return n.loaders = {},
                n
            }
            return n(e, t),
            e.prototype.destroy = function() {
                var e = this.loaders;
                for (var r in e) {
                    var i = e[r];
                    i && i.destroy()
                }
                this.loaders = {},
                t.prototype.destroy.call(this)
            }
            ,
            e.prototype.onFragLoading = function(t) {
                var e = t.frag
                  , r = e.type
                  , i = this.loaders
                  , a = this.hls.config
                  , n = a.fLoader
                  , s = a.loader;
                e.loaded = 0;
                var l = i[r];
                l && (d.b.warn("abort previous fragment loader for type: " + r),
                l.abort()),
                l = i[r] = e.loader = a.fLoader ? new n(a) : new s(a);
                var u = void 0
                  , c = void 0
                  , h = void 0;
                u = {
                    url: e.url,
                    frag: e,
                    responseType: "arraybuffer",
                    progressData: !1
                };
                var f = e.byteRangeStartOffset
                  , p = e.byteRangeEndOffset;
                Object(o.a)(f) && Object(o.a)(p) && (u.rangeStart = f,
                u.rangeEnd = p),
                c = {
                    timeout: a.fragLoadingTimeOut,
                    maxRetry: 0,
                    retryDelay: 0,
                    maxRetryDelay: a.fragLoadingMaxRetryTimeout
                },
                h = {
                    onSuccess: this.loadsuccess.bind(this),
                    onError: this.loaderror.bind(this),
                    onTimeout: this.loadtimeout.bind(this),
                    onProgress: this.loadprogress.bind(this)
                },
                l.load(u, c, h)
            }
            ,
            e.prototype.loadsuccess = function(t, e, r) {
                var i = arguments.length > 3 && void 0 !== arguments[3] ? arguments[3] : null
                  , a = t.data
                  , n = r.frag;
                n.loader = void 0,
                this.loaders[n.type] = void 0,
                this.hls.trigger(s.a.FRAG_LOADED, {
                    payload: a,
                    frag: n,
                    stats: e,
                    networkDetails: i
                })
            }
            ,
            e.prototype.loaderror = function(t, e) {
                var r = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : null
                  , i = e.frag
                  , a = i.loader;
                a && a.abort(),
                this.loaders[i.type] = void 0,
                this.hls.trigger(s.a.ERROR, {
                    type: u.b.NETWORK_ERROR,
                    details: u.a.FRAG_LOAD_ERROR,
                    fatal: !1,
                    frag: e.frag,
                    response: t,
                    networkDetails: r
                })
            }
            ,
            e.prototype.loadtimeout = function(t, e) {
                var r = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : null
                  , i = e.frag
                  , a = i.loader;
                a && a.abort(),
                this.loaders[i.type] = void 0,
                this.hls.trigger(s.a.ERROR, {
                    type: u.b.NETWORK_ERROR,
                    details: u.a.FRAG_LOAD_TIMEOUT,
                    fatal: !1,
                    frag: e.frag,
                    networkDetails: r
                })
            }
            ,
            e.prototype.loadprogress = function(t, e, r) {
                var i = arguments.length > 3 && void 0 !== arguments[3] ? arguments[3] : null
                  , a = e.frag;
                a.loaded = t.loaded,
                this.hls.trigger(s.a.FRAG_LOAD_PROGRESS, {
                    frag: a,
                    stats: t,
                    networkDetails: i
                })
            }
            ,
            e
        }(l.a);
        e.a = c
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(1)
          , s = r(4)
          , l = r(2)
          , u = r(0)
          , d = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, o.a.KEY_LOADING));
                return n.loaders = {},
                n.decryptkey = null,
                n.decrypturl = null,
                n
            }
            return n(e, t),
            e.prototype.destroy = function() {
                for (var t in this.loaders) {
                    var e = this.loaders[t];
                    e && e.destroy()
                }
                this.loaders = {},
                s.a.prototype.destroy.call(this)
            }
            ,
            e.prototype.onKeyLoading = function(t) {
                var e = t.frag
                  , r = e.type
                  , i = this.loaders[r]
                  , a = e.decryptdata
                  , n = a.uri;
                if (n !== this.decrypturl || null === this.decryptkey) {
                    var s = this.hls.config;
                    i && (u.b.warn("abort previous key loader for type:" + r),
                    i.abort()),
                    e.loader = this.loaders[r] = new s.loader(s),
                    this.decrypturl = n,
                    this.decryptkey = null;
                    var l = void 0
                      , d = void 0
                      , c = void 0;
                    l = {
                        url: n,
                        frag: e,
                        responseType: "arraybuffer"
                    },
                    d = {
                        timeout: s.fragLoadingTimeOut,
                        maxRetry: s.fragLoadingMaxRetry,
                        retryDelay: s.fragLoadingRetryDelay,
                        maxRetryDelay: s.fragLoadingMaxRetryTimeout
                    },
                    c = {
                        onSuccess: this.loadsuccess.bind(this),
                        onError: this.loaderror.bind(this),
                        onTimeout: this.loadtimeout.bind(this)
                    },
                    e.loader.load(l, d, c)
                } else
                    this.decryptkey && (a.key = this.decryptkey,
                    this.hls.trigger(o.a.KEY_LOADED, {
                        frag: e
                    }))
            }
            ,
            e.prototype.loadsuccess = function(t, e, r) {
                var i = r.frag;
                this.decryptkey = i.decryptdata.key = new Uint8Array(t.data),
                i.loader = void 0,
                this.loaders[i.type] = void 0,
                this.hls.trigger(o.a.KEY_LOADED, {
                    frag: i
                })
            }
            ,
            e.prototype.loaderror = function(t, e) {
                var r = e.frag
                  , i = r.loader;
                i && i.abort(),
                this.loaders[e.type] = void 0,
                this.hls.trigger(o.a.ERROR, {
                    type: l.b.NETWORK_ERROR,
                    details: l.a.KEY_LOAD_ERROR,
                    fatal: !1,
                    frag: r,
                    response: t
                })
            }
            ,
            e.prototype.loadtimeout = function(t, e) {
                var r = e.frag
                  , i = r.loader;
                i && i.abort(),
                this.loaders[e.type] = void 0,
                this.hls.trigger(o.a.ERROR, {
                    type: l.b.NETWORK_ERROR,
                    details: l.a.KEY_LOAD_TIMEOUT,
                    fatal: !1,
                    frag: r
                })
            }
            ,
            e
        }(s.a);
        e.a = d
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(3)
          , s = r(7)
          , l = r(8)
          , u = r(21)
          , d = r(1)
          , c = r(12)
          , h = r(11)
          , f = r(17)
          , p = r(16)
          , g = r(25)
          , v = r(2)
          , y = r(0)
          , m = r(26)
          , b = r(10)
          , E = r(50)
          , T = r(51)
          , S = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , A = {
            STOPPED: "STOPPED",
            IDLE: "IDLE",
            KEY_LOADING: "KEY_LOADING",
            FRAG_LOADING: "FRAG_LOADING",
            FRAG_LOADING_WAITING_RETRY: "FRAG_LOADING_WAITING_RETRY",
            WAITING_LEVEL: "WAITING_LEVEL",
            PARSING: "PARSING",
            PARSED: "PARSED",
            BUFFER_FLUSHING: "BUFFER_FLUSHING",
            ENDED: "ENDED",
            ERROR: "ERROR"
        }
          , R = function(t) {
            function e(r, n) {
                i(this, e);
                var o = a(this, t.call(this, r, d.a.MEDIA_ATTACHED, d.a.MEDIA_DETACHING, d.a.MANIFEST_LOADING, d.a.MANIFEST_PARSED, d.a.LEVEL_LOADED, d.a.KEY_LOADED, d.a.FRAG_LOADED, d.a.FRAG_LOAD_EMERGENCY_ABORTED, d.a.FRAG_PARSING_INIT_SEGMENT, d.a.FRAG_PARSING_DATA, d.a.FRAG_PARSED, d.a.ERROR, d.a.AUDIO_TRACK_SWITCHING, d.a.AUDIO_TRACK_SWITCHED, d.a.BUFFER_CREATED, d.a.BUFFER_APPENDED, d.a.BUFFER_FLUSHED));
                return o.fragmentTracker = n,
                o.config = r.config,
                o.audioCodecSwap = !1,
                o._state = A.STOPPED,
                o.stallReported = !1,
                o.gapController = null,
                o
            }
            return n(e, t),
            e.prototype.onHandlerDestroying = function() {
                this.stopLoad(),
                t.prototype.onHandlerDestroying.call(this)
            }
            ,
            e.prototype.onHandlerDestroyed = function() {
                this.state = A.STOPPED,
                this.fragmentTracker = null,
                t.prototype.onHandlerDestroyed.call(this)
            }
            ,
            e.prototype.startLoad = function(t) {
                if (this.levels) {
                    var e = this.lastCurrentTime
                      , r = this.hls;
                    if (this.stopLoad(),
                    this.setInterval(100),
                    this.level = -1,
                    this.fragLoadError = 0,
                    !this.startFragRequested) {
                        var i = r.startLevel;
                        -1 === i && (i = 0,
                        this.bitrateTest = !0),
                        this.level = r.nextLoadLevel = i,
                        this.loadedmetadata = !1
                    }
                    e > 0 && -1 === t && (y.b.log("override startPosition with lastCurrentTime @" + e.toFixed(3)),
                    t = e),
                    this.state = A.IDLE,
                    this.nextLoadPosition = this.startPosition = this.lastCurrentTime = t,
                    this.tick()
                } else
                    this.forceStartLoad = !0,
                    this.state = A.STOPPED
            }
            ,
            e.prototype.stopLoad = function() {
                var t = this.fragCurrent;
                t && (t.loader && t.loader.abort(),
                this.fragmentTracker.removeFragment(t),
                this.fragCurrent = null),
                this.fragPrevious = null,
                this.demuxer && (this.demuxer.destroy(),
                this.demuxer = null),
                this.clearInterval(),
                this.state = A.STOPPED,
                this.forceStartLoad = !1
            }
            ,
            e.prototype.doTick = function() {
                switch (this.state) {
                case A.BUFFER_FLUSHING:
                    this.fragLoadError = 0;
                    break;
                case A.IDLE:
                    this._doTickIdle();
                    break;
                case A.WAITING_LEVEL:
                    var t = this.levels[this.level];
                    t && t.details && (this.state = A.IDLE);
                    break;
                case A.FRAG_LOADING_WAITING_RETRY:
                    var e = window.performance.now()
                      , r = this.retryDate;
                    (!r || e >= r || this.media && this.media.seeking) && (y.b.log("mediaController: retryDate reached, switch back to IDLE state"),
                    this.state = A.IDLE);
                    break;
                case A.ERROR:
                case A.STOPPED:
                case A.FRAG_LOADING:
                case A.PARSING:
                case A.PARSED:
                case A.ENDED:
                }
                this._checkBuffer(),
                this._checkFragmentChanged()
            }
            ,
            e.prototype._doTickIdle = function() {
                var t = this.hls
                  , e = t.config
                  , r = this.media;
                if (void 0 !== this.levelLastLoaded && (r || !this.startFragRequested && e.startFragPrefetch)) {
                    var i = void 0;
                    i = this.loadedmetadata ? r.currentTime : this.nextLoadPosition;
                    var a = t.nextLoadLevel
                      , n = this.levels[a];
                    if (n) {
                        var o = n.bitrate
                          , s = void 0;
                        s = o ? Math.max(8 * e.maxBufferSize / o, e.maxBufferLength) : e.maxBufferLength,
                        s = Math.min(s, e.maxMaxBufferLength);
                        var u = l.a.bufferInfo(this.mediaBuffer ? this.mediaBuffer : r, i, e.maxBufferHole)
                          , c = u.len;
                        if (!(c >= s)) {
                            y.b.trace("buffer length of " + c.toFixed(3) + " is below max of " + s.toFixed(3) + ". checking for more payload ..."),
                            this.level = t.nextLoadLevel = a;
                            var h = n.details;
                            if (!h || h.live && this.levelLastLoaded !== a)
                                return void (this.state = A.WAITING_LEVEL);
                            var f = this.fragPrevious;
                            if (!h.live && f && !f.backtracked && f.sn === h.endSN && !u.nextStart) {
                                if (Math.min(r.duration, f.start + f.duration) - Math.max(u.end, f.start) <= Math.max(.2, f.duration)) {
                                    var p = {};
                                    return this.altAudio && (p.type = "video"),
                                    this.hls.trigger(d.a.BUFFER_EOS, p),
                                    void (this.state = A.ENDED)
                                }
                            }
                            this._fetchPayloadOrEos(i, u, h)
                        }
                    }
                }
            }
            ,
            e.prototype._fetchPayloadOrEos = function(t, e, r) {
                var i = this.fragPrevious
                  , a = this.level
                  , n = r.fragments
                  , o = n.length;
                if (0 !== o) {
                    var s = n[0].start
                      , l = n[o - 1].start + n[o - 1].duration
                      , u = e.end
                      , d = void 0;
                    if (r.initSegment && !r.initSegment.data)
                        d = r.initSegment;
                    else if (r.live) {
                        var c = this.config.initialLiveManifestSize;
                        if (o < c)
                            return void y.b.warn("Can not start playback of a level, reason: not enough fragments " + o + " < " + c);
                        if (null === (d = this._ensureFragmentAtLivePoint(r, u, s, l, i, n, o)))
                            return
                    } else
                        u < s && (d = n[0]);
                    d || (d = this._findFragment(s, i, o, n, u, l, r)),
                    d && (d.encrypted ? (y.b.log("Loading key for " + d.sn + " of [" + r.startSN + " ," + r.endSN + "],level " + a),
                    this._loadKey(d)) : (y.b.log("Loading " + d.sn + " of [" + r.startSN + " ," + r.endSN + "],level " + a + ", currentTime:" + t.toFixed(3) + ",bufferEnd:" + u.toFixed(3)),
                    this._loadFragment(d)))
                }
            }
            ,
            e.prototype._ensureFragmentAtLivePoint = function(t, e, r, i, a, n, o) {
                var l = this.hls.config
                  , u = this.media
                  , d = void 0
                  , c = void 0 !== l.liveMaxLatencyDuration ? l.liveMaxLatencyDuration : l.liveMaxLatencyDurationCount * t.targetduration;
                if (e < Math.max(r - l.maxFragLookUpTolerance, i - c)) {
                    var h = this.liveSyncPosition = this.computeLivePosition(r, t);
                    y.b.log("buffer end: " + e.toFixed(3) + " is located too far from the end of live sliding playlist, reset currentTime to : " + h.toFixed(3)),
                    e = h,
                    u && u.readyState && u.duration > h && (u.currentTime = h),
                    this.nextLoadPosition = h
                }
                if (t.PTSKnown && e > i && u && u.readyState)
                    return null;
                if (this.startFragRequested && !t.PTSKnown) {
                    if (a)
                        if (t.hasProgramDateTime)
                            y.b.log("live playlist, switching playlist, load frag with same PDT: " + a.programDateTime),
                            d = Object(E.a)(n, a.endProgramDateTime, l.maxFragLookUpTolerance);
                        else {
                            var f = a.sn + 1;
                            if (f >= t.startSN && f <= t.endSN) {
                                var p = n[f - t.startSN];
                                a.cc === p.cc && (d = p,
                                y.b.log("live playlist, switching playlist, load frag with next SN: " + d.sn))
                            }
                            d || (d = s.a.search(n, function(t) {
                                return a.cc - t.cc
                            })) && y.b.log("live playlist, switching playlist, load frag with same CC: " + d.sn)
                        }
                    d || (d = n[Math.min(o - 1, Math.round(o / 2))],
                    y.b.log("live playlist, switching playlist, unknown, load middle frag : " + d.sn))
                }
                return d
            }
            ,
            e.prototype._findFragment = function(t, e, r, i, a, n, o) {
                var s = this.hls.config
                  , l = void 0;
                if (a < n) {
                    var u = a > n - s.maxFragLookUpTolerance ? 0 : s.maxFragLookUpTolerance;
                    l = Object(E.b)(e, i, a, u)
                } else
                    l = i[r - 1];
                if (l) {
                    var d = l.sn - o.startSN
                      , c = e && l.level === e.level
                      , h = i[d - 1]
                      , f = i[d + 1];
                    if (e && l.sn === e.sn)
                        if (c && !l.backtracked)
                            if (l.sn < o.endSN) {
                                var p = e.deltaPTS;
                                p && p > s.maxBufferHole && e.dropped && d ? (l = h,
                                y.b.warn("SN just loaded, with large PTS gap between audio and video, maybe frag is not starting with a keyframe ? load previous one to try to overcome this")) : (l = f,
                                y.b.log("SN just loaded, load next one: " + l.sn, l))
                            } else
                                l = null;
                        else
                            l.backtracked && (f && f.backtracked ? (y.b.warn("Already backtracked from fragment " + f.sn + ", will not backtrack to fragment " + l.sn + ". Loading fragment " + f.sn),
                            l = f) : (y.b.warn("Loaded fragment with dropped frames, backtracking 1 segment to find a keyframe"),
                            l.dropped = 0,
                            h ? (l = h,
                            l.backtracked = !0) : d && (l = null)))
                }
                return l
            }
            ,
            e.prototype._loadKey = function(t) {
                this.state = A.KEY_LOADING,
                this.hls.trigger(d.a.KEY_LOADING, {
                    frag: t
                })
            }
            ,
            e.prototype._loadFragment = function(t) {
                var e = this.fragmentTracker.getState(t);
                this.fragCurrent = t,
                this.startFragRequested = !0,
                Object(o.a)(t.sn) && !t.bitrateTest && (this.nextLoadPosition = t.start + t.duration),
                t.backtracked || e === c.a.NOT_LOADED || e === c.a.PARTIAL ? (t.autoLevel = this.hls.autoLevelEnabled,
                t.bitrateTest = this.bitrateTest,
                this.hls.trigger(d.a.FRAG_LOADING, {
                    frag: t
                }),
                this.demuxer || (this.demuxer = new u.a(this.hls,"main")),
                this.state = A.FRAG_LOADING) : e === c.a.APPENDING && this._reduceMaxBufferLength(t.duration) && this.fragmentTracker.removeFragment(t)
            }
            ,
            e.prototype.getBufferedFrag = function(t) {
                return this.fragmentTracker.getBufferedFrag(t, f.a.LevelType.MAIN)
            }
            ,
            e.prototype.followingBufferedFrag = function(t) {
                return t ? this.getBufferedFrag(t.endPTS + .5) : null
            }
            ,
            e.prototype._checkFragmentChanged = function() {
                var t = void 0
                  , e = void 0
                  , r = this.media;
                if (r && r.readyState && !1 === r.seeking && (e = r.currentTime,
                e > this.lastCurrentTime && (this.lastCurrentTime = e),
                l.a.isBuffered(r, e) ? t = this.getBufferedFrag(e) : l.a.isBuffered(r, e + .1) && (t = this.getBufferedFrag(e + .1)),
                t)) {
                    var i = t;
                    if (i !== this.fragPlaying) {
                        this.hls.trigger(d.a.FRAG_CHANGED, {
                            frag: i
                        });
                        var a = i.level;
                        this.fragPlaying && this.fragPlaying.level === a || this.hls.trigger(d.a.LEVEL_SWITCHED, {
                            level: a
                        }),
                        this.fragPlaying = i
                    }
                }
            }
            ,
            e.prototype.immediateLevelSwitch = function() {
                if (y.b.log("immediateLevelSwitch"),
                !this.immediateSwitch) {
                    this.immediateSwitch = !0;
                    var t = this.media
                      , e = void 0;
                    t ? (e = t.paused,
                    t.pause()) : e = !0,
                    this.previouslyPaused = e
                }
                var r = this.fragCurrent;
                r && r.loader && r.loader.abort(),
                this.fragCurrent = null,
                this.flushMainBuffer(0, Number.POSITIVE_INFINITY)
            }
            ,
            e.prototype.immediateLevelSwitchEnd = function() {
                var t = this.media;
                t && t.buffered.length && (this.immediateSwitch = !1,
                l.a.isBuffered(t, t.currentTime) && (t.currentTime -= 1e-4),
                this.previouslyPaused || t.play())
            }
            ,
            e.prototype.nextLevelSwitch = function() {
                var t = this.media;
                if (t && t.readyState) {
                    var e = void 0
                      , r = void 0
                      , i = void 0;
                    if (r = this.getBufferedFrag(t.currentTime),
                    r && r.startPTS > 1 && this.flushMainBuffer(0, r.startPTS - 1),
                    t.paused)
                        e = 0;
                    else {
                        var a = this.hls.nextLoadLevel
                          , n = this.levels[a]
                          , o = this.fragLastKbps;
                        e = o && this.fragCurrent ? this.fragCurrent.duration * n.bitrate / (1e3 * o) + 1 : 0
                    }
                    if ((i = this.getBufferedFrag(t.currentTime + e)) && (i = this.followingBufferedFrag(i))) {
                        var s = this.fragCurrent;
                        s && s.loader && s.loader.abort(),
                        this.fragCurrent = null,
                        this.flushMainBuffer(i.maxStartPTS, Number.POSITIVE_INFINITY)
                    }
                }
            }
            ,
            e.prototype.flushMainBuffer = function(t, e) {
                this.state = A.BUFFER_FLUSHING;
                var r = {
                    startOffset: t,
                    endOffset: e
                };
                this.altAudio && (r.type = "video"),
                this.hls.trigger(d.a.BUFFER_FLUSHING, r)
            }
            ,
            e.prototype.onMediaAttached = function(t) {
                var e = this.media = this.mediaBuffer = t.media;
                this.onvseeking = this.onMediaSeeking.bind(this),
                this.onvseeked = this.onMediaSeeked.bind(this),
                this.onvended = this.onMediaEnded.bind(this),
                e.addEventListener("seeking", this.onvseeking),
                e.addEventListener("seeked", this.onvseeked),
                e.addEventListener("ended", this.onvended);
                var r = this.config;
                this.levels && r.autoStartLoad && this.hls.startLoad(r.startPosition),
                this.gapController = new T.a(r,e,this.fragmentTracker,this.hls)
            }
            ,
            e.prototype.onMediaDetaching = function() {
                var t = this.media;
                t && t.ended && (y.b.log("MSE detaching and video ended, reset startPosition"),
                this.startPosition = this.lastCurrentTime = 0);
                var e = this.levels;
                e && e.forEach(function(t) {
                    t.details && t.details.fragments.forEach(function(t) {
                        t.backtracked = void 0
                    })
                }),
                t && (t.removeEventListener("seeking", this.onvseeking),
                t.removeEventListener("seeked", this.onvseeked),
                t.removeEventListener("ended", this.onvended),
                this.onvseeking = this.onvseeked = this.onvended = null),
                this.media = this.mediaBuffer = null,
                this.loadedmetadata = !1,
                this.stopLoad()
            }
            ,
            e.prototype.onMediaSeeking = function() {
                var t = this.media
                  , e = t ? t.currentTime : void 0
                  , r = this.config;
                Object(o.a)(e) && y.b.log("media seeking to " + e.toFixed(3));
                var i = this.mediaBuffer ? this.mediaBuffer : t
                  , a = l.a.bufferInfo(i, e, this.config.maxBufferHole);
                if (this.state === A.FRAG_LOADING) {
                    var n = this.fragCurrent;
                    if (0 === a.len && n) {
                        var s = r.maxFragLookUpTolerance
                          , u = n.start - s
                          , d = n.start + n.duration + s;
                        e < u || e > d ? (n.loader && (y.b.log("seeking outside of buffer while fragment load in progress, cancel fragment load"),
                        n.loader.abort()),
                        this.fragCurrent = null,
                        this.fragPrevious = null,
                        this.state = A.IDLE) : y.b.log("seeking outside of buffer but within currently loaded fragment range")
                    }
                } else
                    this.state === A.ENDED && (0 === a.len && (this.fragPrevious = 0),
                    this.state = A.IDLE);
                t && (this.lastCurrentTime = e),
                this.loadedmetadata || (this.nextLoadPosition = this.startPosition = e),
                this.tick()
            }
            ,
            e.prototype.onMediaSeeked = function() {
                var t = this.media
                  , e = t ? t.currentTime : void 0;
                Object(o.a)(e) && y.b.log("media seeked to " + e.toFixed(3)),
                this.tick()
            }
            ,
            e.prototype.onMediaEnded = function() {
                y.b.log("media ended"),
                this.startPosition = this.lastCurrentTime = 0
            }
            ,
            e.prototype.onManifestLoading = function() {
                y.b.log("trigger BUFFER_RESET"),
                this.hls.trigger(d.a.BUFFER_RESET),
                this.fragmentTracker.removeAllFragments(),
                this.stalled = !1,
                this.startPosition = this.lastCurrentTime = 0
            }
            ,
            e.prototype.onManifestParsed = function(t) {
                var e = !1
                  , r = !1
                  , i = void 0;
                t.levels.forEach(function(t) {
                    (i = t.audioCodec) && (-1 !== i.indexOf("mp4a.40.2") && (e = !0),
                    -1 !== i.indexOf("mp4a.40.5") && (r = !0))
                }),
                this.audioCodecSwitch = e && r,
                this.audioCodecSwitch && y.b.log("both AAC/HE-AAC audio found in levels; declaring level codec as HE-AAC"),
                this.levels = t.levels,
                this.startFragRequested = !1;
                var a = this.config;
                (a.autoStartLoad || this.forceStartLoad) && this.hls.startLoad(a.startPosition)
            }
            ,
            e.prototype.onLevelLoaded = function(t) {
                var e = t.details
                  , r = t.level
                  , i = this.levels[this.levelLastLoaded]
                  , a = this.levels[r]
                  , n = e.totalduration
                  , s = 0;
                if (y.b.log("level " + r + " loaded [" + e.startSN + "," + e.endSN + "],duration:" + n),
                e.live) {
                    var l = a.details;
                    l && e.fragments.length > 0 ? (p.b(l, e),
                    s = e.fragments[0].start,
                    this.liveSyncPosition = this.computeLivePosition(s, l),
                    e.PTSKnown && Object(o.a)(s) ? y.b.log("live playlist sliding:" + s.toFixed(3)) : (y.b.log("live playlist - outdated PTS, unknown sliding"),
                    Object(m.a)(this.fragPrevious, i, e))) : (y.b.log("live playlist - first load, unknown sliding"),
                    e.PTSKnown = !1,
                    Object(m.a)(this.fragPrevious, i, e))
                } else
                    e.PTSKnown = !1;
                if (a.details = e,
                this.levelLastLoaded = r,
                this.hls.trigger(d.a.LEVEL_UPDATED, {
                    details: e,
                    level: r
                }),
                !1 === this.startFragRequested) {
                    if (-1 === this.startPosition || -1 === this.lastCurrentTime) {
                        var u = e.startTimeOffset;
                        Object(o.a)(u) ? (u < 0 && (y.b.log("negative start time offset " + u + ", count from end of last fragment"),
                        u = s + n + u),
                        y.b.log("start time offset found in playlist, adjust startPosition to " + u),
                        this.startPosition = u) : e.live ? (this.startPosition = this.computeLivePosition(s, e),
                        y.b.log("configure startPosition to " + this.startPosition)) : this.startPosition = 0,
                        this.lastCurrentTime = this.startPosition
                    }
                    this.nextLoadPosition = this.startPosition
                }
                this.state === A.WAITING_LEVEL && (this.state = A.IDLE),
                this.tick()
            }
            ,
            e.prototype.onKeyLoaded = function() {
                this.state === A.KEY_LOADING && (this.state = A.IDLE,
                this.tick())
            }
            ,
            e.prototype.onFragLoaded = function(t) {
                var e = this.fragCurrent
                  , r = this.hls
                  , i = this.levels
                  , a = this.media
                  , n = t.frag;
                if (this.state === A.FRAG_LOADING && e && "main" === n.type && n.level === e.level && n.sn === e.sn) {
                    var o = t.stats
                      , s = i[e.level]
                      , l = s.details;
                    if (this.bitrateTest = !1,
                    this.stats = o,
                    y.b.log("Loaded " + e.sn + " of [" + l.startSN + " ," + l.endSN + "],level " + e.level),
                    n.bitrateTest && r.nextLoadLevel)
                        this.state = A.IDLE,
                        this.startFragRequested = !1,
                        o.tparsed = o.tbuffered = window.performance.now(),
                        r.trigger(d.a.FRAG_BUFFERED, {
                            stats: o,
                            frag: e,
                            id: "main"
                        }),
                        this.tick();
                    else if ("initSegment" === n.sn)
                        this.state = A.IDLE,
                        o.tparsed = o.tbuffered = window.performance.now(),
                        l.initSegment.data = t.payload,
                        r.trigger(d.a.FRAG_BUFFERED, {
                            stats: o,
                            frag: e,
                            id: "main"
                        }),
                        this.tick();
                    else {
                        y.b.log("Parsing " + e.sn + " of [" + l.startSN + " ," + l.endSN + "],level " + e.level + ", cc " + e.cc),
                        this.state = A.PARSING,
                        this.pendingBuffering = !0,
                        this.appended = !1,
                        n.bitrateTest && (n.bitrateTest = !1,
                        this.fragmentTracker.onFragLoaded({
                            frag: n
                        }));
                        var c = !(a && a.seeking) && (l.PTSKnown || !l.live)
                          , h = l.initSegment ? l.initSegment.data : []
                          , f = this._getAudioCodec(s)
                          , p = this.demuxer = this.demuxer || new u.a(this.hls,"main");
                        p.push(t.payload, h, f, s.videoCodec, e, l.totalduration, c)
                    }
                }
                this.fragLoadError = 0
            }
            ,
            e.prototype.onFragParsingInitSegment = function(t) {
                var e = this.fragCurrent
                  , r = t.frag;
                if (e && "main" === t.id && r.sn === e.sn && r.level === e.level && this.state === A.PARSING) {
                    var i = t.tracks
                      , a = void 0
                      , n = void 0;
                    if (i.audio && this.altAudio && delete i.audio,
                    n = i.audio) {
                        var o = this.levels[this.level].audioCodec
                          , s = navigator.userAgent.toLowerCase();
                        o && this.audioCodecSwap && (y.b.log("swapping playlist audio codec"),
                        o = -1 !== o.indexOf("mp4a.40.5") ? "mp4a.40.2" : "mp4a.40.5"),
                        this.audioCodecSwitch && 1 !== n.metadata.channelCount && -1 === s.indexOf("firefox") && (o = "mp4a.40.5"),
                        -1 !== s.indexOf("android") && "audio/mpeg" !== n.container && (o = "mp4a.40.2",
                        y.b.log("Android: force audio codec to " + o)),
                        n.levelCodec = o,
                        n.id = t.id
                    }
                    n = i.video,
                    n && (n.levelCodec = this.levels[this.level].videoCodec,
                    n.id = t.id),
                    this.hls.trigger(d.a.BUFFER_CODECS, i);
                    for (a in i) {
                        n = i[a],
                        y.b.log("main track:" + a + ",container:" + n.container + ",codecs[level/parsed]=[" + n.levelCodec + "/" + n.codec + "]");
                        var l = n.initSegment;
                        l && (this.appended = !0,
                        this.pendingBuffering = !0,
                        this.hls.trigger(d.a.BUFFER_APPENDING, {
                            type: a,
                            data: l,
                            parent: "main",
                            content: "initSegment"
                        }))
                    }
                    this.tick()
                }
            }
            ,
            e.prototype.onFragParsingData = function(t) {
                var e = this
                  , r = this.fragCurrent
                  , i = t.frag;
                if (r && "main" === t.id && i.sn === r.sn && i.level === r.level && ("audio" !== t.type || !this.altAudio) && this.state === A.PARSING) {
                    var a = this.levels[this.level]
                      , n = r;
                    if (Object(o.a)(t.endPTS) || (t.endPTS = t.startPTS + r.duration,
                    t.endDTS = t.startDTS + r.duration),
                    !0 === t.hasAudio && n.addElementaryStream(h.a.ElementaryStreamTypes.AUDIO),
                    !0 === t.hasVideo && n.addElementaryStream(h.a.ElementaryStreamTypes.VIDEO),
                    y.b.log("Parsed " + t.type + ",PTS:[" + t.startPTS.toFixed(3) + "," + t.endPTS.toFixed(3) + "],DTS:[" + t.startDTS.toFixed(3) + "/" + t.endDTS.toFixed(3) + "],nb:" + t.nb + ",dropped:" + (t.dropped || 0)),
                    "video" === t.type)
                        if (n.dropped = t.dropped,
                        n.dropped)
                            if (n.backtracked)
                                y.b.warn("Already backtracked on this fragment, appending with the gap", n.sn);
                            else {
                                var s = a.details;
                                if (!s || n.sn !== s.startSN)
                                    return y.b.warn("missing video frame(s), backtracking fragment", n.sn),
                                    this.fragmentTracker.removeFragment(n),
                                    n.backtracked = !0,
                                    this.nextLoadPosition = t.startPTS,
                                    this.state = A.IDLE,
                                    this.fragPrevious = n,
                                    void this.tick();
                                y.b.warn("missing video frame(s) on first frag, appending with gap", n.sn)
                            }
                        else
                            n.backtracked = !1;
                    var l = p.c(a.details, n, t.startPTS, t.endPTS, t.startDTS, t.endDTS)
                      , u = this.hls;
                    u.trigger(d.a.LEVEL_PTS_UPDATED, {
                        details: a.details,
                        level: this.level,
                        drift: l,
                        type: t.type,
                        start: t.startPTS,
                        end: t.endPTS
                    }),
                    [t.data1, t.data2].forEach(function(r) {
                        r && r.length && e.state === A.PARSING && (e.appended = !0,
                        e.pendingBuffering = !0,
                        u.trigger(d.a.BUFFER_APPENDING, {
                            type: t.type,
                            data: r,
                            parent: "main",
                            content: "data"
                        }))
                    }),
                    this.tick()
                }
            }
            ,
            e.prototype.onFragParsed = function(t) {
                var e = this.fragCurrent
                  , r = t.frag;
                e && "main" === t.id && r.sn === e.sn && r.level === e.level && this.state === A.PARSING && (this.stats.tparsed = window.performance.now(),
                this.state = A.PARSED,
                this._checkAppendedParsed())
            }
            ,
            e.prototype.onAudioTrackSwitching = function(t) {
                var e = !!t.url
                  , r = t.id;
                if (!e) {
                    if (this.mediaBuffer !== this.media) {
                        y.b.log("switching on main audio, use media.buffered to schedule main fragment loading"),
                        this.mediaBuffer = this.media;
                        var i = this.fragCurrent;
                        i.loader && (y.b.log("switching to main audio track, cancel main fragment load"),
                        i.loader.abort()),
                        this.fragCurrent = null,
                        this.fragPrevious = null,
                        this.demuxer && (this.demuxer.destroy(),
                        this.demuxer = null),
                        this.state = A.IDLE
                    }
                    var a = this.hls;
                    a.trigger(d.a.BUFFER_FLUSHING, {
                        startOffset: 0,
                        endOffset: Number.POSITIVE_INFINITY,
                        type: "audio"
                    }),
                    a.trigger(d.a.AUDIO_TRACK_SWITCHED, {
                        id: r
                    }),
                    this.altAudio = !1
                }
            }
            ,
            e.prototype.onAudioTrackSwitched = function(t) {
                var e = t.id
                  , r = !!this.hls.audioTracks[e].url;
                if (r) {
                    var i = this.videoBuffer;
                    i && this.mediaBuffer !== i && (y.b.log("switching on alternate audio, use video.buffered to schedule main fragment loading"),
                    this.mediaBuffer = i)
                }
                this.altAudio = r,
                this.tick()
            }
            ,
            e.prototype.onBufferCreated = function(t) {
                var e = t.tracks
                  , r = void 0
                  , i = void 0
                  , a = !1;
                for (var n in e) {
                    var o = e[n];
                    "main" === o.id ? (i = n,
                    r = o,
                    "video" === n && (this.videoBuffer = e[n].buffer)) : a = !0
                }
                a && r ? (y.b.log("alternate track found, use " + i + ".buffered to schedule main fragment loading"),
                this.mediaBuffer = r.buffer) : this.mediaBuffer = this.media
            }
            ,
            e.prototype.onBufferAppended = function(t) {
                if ("main" === t.parent) {
                    var e = this.state;
                    e !== A.PARSING && e !== A.PARSED || (this.pendingBuffering = t.pending > 0,
                    this._checkAppendedParsed())
                }
            }
            ,
            e.prototype._checkAppendedParsed = function() {
                if (!(this.state !== A.PARSED || this.appended && this.pendingBuffering)) {
                    var t = this.fragCurrent;
                    if (t) {
                        var e = this.mediaBuffer ? this.mediaBuffer : this.media;
                        y.b.log("main buffered : " + g.a.toString(e.buffered)),
                        this.fragPrevious = t;
                        var r = this.stats;
                        r.tbuffered = window.performance.now(),
                        this.fragLastKbps = Math.round(8 * r.total / (r.tbuffered - r.tfirst)),
                        this.hls.trigger(d.a.FRAG_BUFFERED, {
                            stats: r,
                            frag: t,
                            id: "main"
                        }),
                        this.state = A.IDLE
                    }
                    this.tick()
                }
            }
            ,
            e.prototype.onError = function(t) {
                var e = t.frag || this.fragCurrent;
                if (!e || "main" === e.type) {
                    var r = !!this.media && l.a.isBuffered(this.media, this.media.currentTime) && l.a.isBuffered(this.media, this.media.currentTime + .5);
                    switch (t.details) {
                    case v.a.FRAG_LOAD_ERROR:
                    case v.a.FRAG_LOAD_TIMEOUT:
                    case v.a.KEY_LOAD_ERROR:
                    case v.a.KEY_LOAD_TIMEOUT:
                        if (!t.fatal)
                            if (this.fragLoadError + 1 <= this.config.fragLoadingMaxRetry) {
                                var i = Math.min(Math.pow(2, this.fragLoadError) * this.config.fragLoadingRetryDelay, this.config.fragLoadingMaxRetryTimeout);
                                y.b.warn("mediaController: frag loading failed, retry in " + i + " ms"),
                                this.retryDate = window.performance.now() + i,
                                this.loadedmetadata || (this.startFragRequested = !1,
                                this.nextLoadPosition = this.startPosition),
                                this.fragLoadError++,
                                this.state = A.FRAG_LOADING_WAITING_RETRY
                            } else
                                y.b.error("mediaController: " + t.details + " reaches max retry, redispatch as fatal ..."),
                                t.fatal = !0,
                                this.state = A.ERROR;
                        break;
                    case v.a.LEVEL_LOAD_ERROR:
                    case v.a.LEVEL_LOAD_TIMEOUT:
                        this.state !== A.ERROR && (t.fatal ? (this.state = A.ERROR,
                        y.b.warn("streamController: " + t.details + ",switch to " + this.state + " state ...")) : t.levelRetry || this.state !== A.WAITING_LEVEL || (this.state = A.IDLE));
                        break;
                    case v.a.BUFFER_FULL_ERROR:
                        "main" !== t.parent || this.state !== A.PARSING && this.state !== A.PARSED || (r ? (this._reduceMaxBufferLength(this.config.maxBufferLength),
                        this.state = A.IDLE) : (y.b.warn("buffer full error also media.currentTime is not buffered, flush everything"),
                        this.fragCurrent = null,
                        this.flushMainBuffer(0, Number.POSITIVE_INFINITY)))
                    }
                }
            }
            ,
            e.prototype._reduceMaxBufferLength = function(t) {
                var e = this.config;
                return e.maxMaxBufferLength >= t && (e.maxMaxBufferLength /= 2,
                y.b.warn("main:reduce max buffer length to " + e.maxMaxBufferLength + "s"),
                !0)
            }
            ,
            e.prototype._checkBuffer = function() {
                var t = this.media;
                if (t && 0 !== t.readyState) {
                    var e = this.mediaBuffer ? this.mediaBuffer : t
                      , r = e.buffered;
                    !this.loadedmetadata && r.length ? (this.loadedmetadata = !0,
                    this._seekToStartPos()) : this.immediateSwitch ? this.immediateLevelSwitchEnd() : this.gapController.poll(this.lastCurrentTime, r)
                }
            }
            ,
            e.prototype.onFragLoadEmergencyAborted = function() {
                this.state = A.IDLE,
                this.loadedmetadata || (this.startFragRequested = !1,
                this.nextLoadPosition = this.startPosition),
                this.tick()
            }
            ,
            e.prototype.onBufferFlushed = function() {
                var t = this.mediaBuffer ? this.mediaBuffer : this.media;
                t && this.fragmentTracker.detectEvictedFragments(h.a.ElementaryStreamTypes.VIDEO, t.buffered),
                this.state = A.IDLE,
                this.fragPrevious = null
            }
            ,
            e.prototype.swapAudioCodec = function() {
                this.audioCodecSwap = !this.audioCodecSwap
            }
            ,
            e.prototype.computeLivePosition = function(t, e) {
                var r = void 0 !== this.config.liveSyncDuration ? this.config.liveSyncDuration : this.config.liveSyncDurationCount * e.targetduration;
                return t + Math.max(0, e.totalduration - r)
            }
            ,
            e.prototype._seekToStartPos = function() {
                var t = this.media
                  , e = t.currentTime
                  , r = t.seeking ? e : this.startPosition;
                e !== r && (y.b.log("target start position not buffered, seek to buffered.start(0) " + r + " from current time " + e + " "),
                t.currentTime = r)
            }
            ,
            e.prototype._getAudioCodec = function(t) {
                var e = this.config.defaultAudioCodec || t.audioCodec;
                return this.audioCodecSwap && (y.b.log("swapping playlist audio codec"),
                e && (e = -1 !== e.indexOf("mp4a.40.5") ? "mp4a.40.2" : "mp4a.40.5")),
                e
            }
            ,
            S(e, [{
                key: "state",
                set: function(t) {
                    if (this.state !== t) {
                        var e = this.state;
                        this._state = t,
                        y.b.log("main stream:" + e + "->" + t),
                        this.hls.trigger(d.a.STREAM_STATE_TRANSITION, {
                            previousState: e,
                            nextState: t
                        })
                    }
                },
                get: function() {
                    return this._state
                }
            }, {
                key: "currentLevel",
                get: function() {
                    var t = this.media;
                    if (t) {
                        var e = this.getBufferedFrag(t.currentTime);
                        if (e)
                            return e.level
                    }
                    return -1
                }
            }, {
                key: "nextBufferedFrag",
                get: function() {
                    var t = this.media;
                    return t ? this.followingBufferedFrag(this.getBufferedFrag(t.currentTime)) : null
                }
            }, {
                key: "nextLevel",
                get: function() {
                    var t = this.nextBufferedFrag;
                    return t ? t.level : -1
                }
            }, {
                key: "liveSyncPosition",
                get: function() {
                    return this._liveSyncPosition
                },
                set: function(t) {
                    this._liveSyncPosition = t
                }
            }]),
            e
        }(b.a);
        e.a = R
    }
    , function(t, e, r) {
        function i(t) {
            function e(i) {
                if (r[i])
                    return r[i].exports;
                var a = r[i] = {
                    i: i,
                    l: !1,
                    exports: {}
                };
                return t[i].call(a.exports, a, a.exports, e),
                a.l = !0,
                a.exports
            }
            var r = {};
            e.m = t,
            e.c = r,
            e.i = function(t) {
                return t
            }
            ,
            e.d = function(t, r, i) {
                e.o(t, r) || Object.defineProperty(t, r, {
                    configurable: !1,
                    enumerable: !0,
                    get: i
                })
            }
            ,
            e.n = function(t) {
                var r = t && t.__esModule ? function() {
                    return t.default
                }
                : function() {
                    return t
                }
                ;
                return e.d(r, "a", r),
                r
            }
            ,
            e.o = function(t, e) {
                return Object.prototype.hasOwnProperty.call(t, e)
            }
            ,
            e.p = "/",
            e.oe = function(t) {
                throw console.error(t),
                t
            }
            ;
            var i = e(e.s = ENTRY_MODULE);
            return i.default || i
        }
        function a(t) {
            return (t + "").replace(/[.?*+^$[\]\\(){}|-]/g, "\\$&")
        }
        function n(t, e, i) {
            var n = {};
            n[i] = [];
            var o = e.toString()
              , s = o.match(/^function\s?\(\w+,\s*\w+,\s*(\w+)\)/);
            if (!s)
                return n;
            for (var d, c = s[1], h = new RegExp("(\\\\n|\\W)" + a(c) + u,"g"); d = h.exec(o); )
                "dll-reference" !== d[3] && n[i].push(d[3]);
            for (h = new RegExp("\\(" + a(c) + '\\("(dll-reference\\s(' + l + '))"\\)\\)' + u,"g"); d = h.exec(o); )
                t[d[2]] || (n[i].push(d[1]),
                t[d[2]] = r(d[1]).m),
                n[d[2]] = n[d[2]] || [],
                n[d[2]].push(d[4]);
            return n
        }
        function o(t) {
            return Object.keys(t).reduce(function(e, r) {
                return e || t[r].length > 0
            }, !1)
        }
        function s(t, e) {
            for (var r = {
                main: [e]
            }, i = {
                main: []
            }, a = {
                main: {}
            }; o(r); )
                for (var s = Object.keys(r), l = 0; l < s.length; l++) {
                    var u = s[l]
                      , d = r[u]
                      , c = d.pop();
                    if (a[u] = a[u] || {},
                    !a[u][c] && t[u][c]) {
                        a[u][c] = !0,
                        i[u] = i[u] || [],
                        i[u].push(c);
                        for (var h = n(t, t[u][c], u), f = Object.keys(h), p = 0; p < f.length; p++)
                            r[f[p]] = r[f[p]] || [],
                            r[f[p]] = r[f[p]].concat(h[f[p]])
                    }
                }
            return i
        }
        var l = "[\\.|\\-|\\+|\\w|/|@]+"
          , u = "\\((/\\*.*?\\*/)?s?.*?(" + l + ").*?\\)";
        t.exports = function(t, e) {
            e = e || {};
            var a = {
                main: r.m
            }
              , n = e.all ? {
                main: Object.keys(a)
            } : s(a, t)
              , o = "";
            Object.keys(n).filter(function(t) {
                return "main" !== t
            }).forEach(function(t) {
                for (var e = 0; n[t][e]; )
                    e++;
                n[t].push(e),
                a[t][e] = "(function(module, exports, __webpack_require__) { module.exports = __webpack_require__; })",
                o = o + "var " + t + " = (" + i.toString().replace("ENTRY_MODULE", JSON.stringify(e)) + ")({" + n[t].map(function(e) {
                    return JSON.stringify(e) + ": " + a[t][e].toString()
                }).join(",") + "});\n"
            }),
            o = o + "(" + i.toString().replace("ENTRY_MODULE", JSON.stringify(t)) + ")({" + n.main.map(function(t) {
                return JSON.stringify(t) + ": " + a.main[t].toString()
            }).join(",") + "})(self);";
            var l = new window.Blob([o],{
                type: "text/javascript"
            });
            if (e.bare)
                return l;
            var u = window.URL || window.webkitURL || window.mozURL || window.msURL
              , d = u.createObjectURL(l)
              , c = new window.Worker(d);
            return c.objectURL = d,
            c
        }
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = function() {
            function t(e, r) {
                i(this, t),
                this.subtle = e,
                this.aesIV = r
            }
            return t.prototype.decrypt = function(t, e) {
                return this.subtle.decrypt({
                    name: "AES-CBC",
                    iv: this.aesIV
                }, e, t)
            }
            ,
            t
        }();
        e.a = a
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = function() {
            function t(e, r) {
                i(this, t),
                this.subtle = e,
                this.key = r
            }
            return t.prototype.expandKey = function() {
                return this.subtle.importKey("raw", this.key, {
                    name: "AES-CBC"
                }, !1, ["encrypt", "decrypt"])
            }
            ,
            t
        }();
        e.a = a
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t) {
            var e = t.byteLength
              , r = e && new DataView(t).getUint8(e - 1);
            return r ? t.slice(0, e - r) : t
        }
        var n = function() {
            function t() {
                i(this, t),
                this.rcon = [0, 1, 2, 4, 8, 16, 32, 64, 128, 27, 54],
                this.subMix = [new Uint32Array(256), new Uint32Array(256), new Uint32Array(256), new Uint32Array(256)],
                this.invSubMix = [new Uint32Array(256), new Uint32Array(256), new Uint32Array(256), new Uint32Array(256)],
                this.sBox = new Uint32Array(256),
                this.invSBox = new Uint32Array(256),
                this.key = new Uint32Array(0),
                this.initTable()
            }
            return t.prototype.uint8ArrayToUint32Array_ = function(t) {
                for (var e = new DataView(t), r = new Uint32Array(4), i = 0; i < 4; i++)
                    r[i] = e.getUint32(4 * i);
                return r
            }
            ,
            t.prototype.initTable = function() {
                var t = this.sBox
                  , e = this.invSBox
                  , r = this.subMix
                  , i = r[0]
                  , a = r[1]
                  , n = r[2]
                  , o = r[3]
                  , s = this.invSubMix
                  , l = s[0]
                  , u = s[1]
                  , d = s[2]
                  , c = s[3]
                  , h = new Uint32Array(256)
                  , f = 0
                  , p = 0
                  , g = 0;
                for (g = 0; g < 256; g++)
                    h[g] = g < 128 ? g << 1 : g << 1 ^ 283;
                for (g = 0; g < 256; g++) {
                    var v = p ^ p << 1 ^ p << 2 ^ p << 3 ^ p << 4;
                    v = v >>> 8 ^ 255 & v ^ 99,
                    t[f] = v,
                    e[v] = f;
                    var y = h[f]
                      , m = h[y]
                      , b = h[m]
                      , E = 257 * h[v] ^ 16843008 * v;
                    i[f] = E << 24 | E >>> 8,
                    a[f] = E << 16 | E >>> 16,
                    n[f] = E << 8 | E >>> 24,
                    o[f] = E,
                    E = 16843009 * b ^ 65537 * m ^ 257 * y ^ 16843008 * f,
                    l[v] = E << 24 | E >>> 8,
                    u[v] = E << 16 | E >>> 16,
                    d[v] = E << 8 | E >>> 24,
                    c[v] = E,
                    f ? (f = y ^ h[h[h[b ^ y]]],
                    p ^= h[h[p]]) : f = p = 1
                }
            }
            ,
            t.prototype.expandKey = function(t) {
                for (var e = this.uint8ArrayToUint32Array_(t), r = !0, i = 0; i < e.length && r; )
                    r = e[i] === this.key[i],
                    i++;
                if (!r) {
                    this.key = e;
                    var a = this.keySize = e.length;
                    if (4 !== a && 6 !== a && 8 !== a)
                        throw new Error("Invalid aes key size=" + a);
                    var n = this.ksRows = 4 * (a + 6 + 1)
                      , o = void 0
                      , s = void 0
                      , l = this.keySchedule = new Uint32Array(n)
                      , u = this.invKeySchedule = new Uint32Array(n)
                      , d = this.sBox
                      , c = this.rcon
                      , h = this.invSubMix
                      , f = h[0]
                      , p = h[1]
                      , g = h[2]
                      , v = h[3]
                      , y = void 0
                      , m = void 0;
                    for (o = 0; o < n; o++)
                        o < a ? y = l[o] = e[o] : (m = y,
                        o % a == 0 ? (m = m << 8 | m >>> 24,
                        m = d[m >>> 24] << 24 | d[m >>> 16 & 255] << 16 | d[m >>> 8 & 255] << 8 | d[255 & m],
                        m ^= c[o / a | 0] << 24) : a > 6 && o % a == 4 && (m = d[m >>> 24] << 24 | d[m >>> 16 & 255] << 16 | d[m >>> 8 & 255] << 8 | d[255 & m]),
                        l[o] = y = (l[o - a] ^ m) >>> 0);
                    for (s = 0; s < n; s++)
                        o = n - s,
                        m = 3 & s ? l[o] : l[o - 4],
                        u[s] = s < 4 || o <= 4 ? m : f[d[m >>> 24]] ^ p[d[m >>> 16 & 255]] ^ g[d[m >>> 8 & 255]] ^ v[d[255 & m]],
                        u[s] = u[s] >>> 0
                }
            }
            ,
            t.prototype.networkToHostOrderSwap = function(t) {
                return t << 24 | (65280 & t) << 8 | (16711680 & t) >> 8 | t >>> 24
            }
            ,
            t.prototype.decrypt = function(t, e, r, i) {
                for (var n = this.keySize + 6, o = this.invKeySchedule, s = this.invSBox, l = this.invSubMix, u = l[0], d = l[1], c = l[2], h = l[3], f = this.uint8ArrayToUint32Array_(r), p = f[0], g = f[1], v = f[2], y = f[3], m = new Int32Array(t), b = new Int32Array(m.length), E = void 0, T = void 0, S = void 0, A = void 0, R = void 0, _ = void 0, w = void 0, L = void 0, D = void 0, I = void 0, k = void 0, O = void 0, C = void 0, P = void 0, x = this.networkToHostOrderSwap; e < m.length; ) {
                    for (D = x(m[e]),
                    I = x(m[e + 1]),
                    k = x(m[e + 2]),
                    O = x(m[e + 3]),
                    R = D ^ o[0],
                    _ = O ^ o[1],
                    w = k ^ o[2],
                    L = I ^ o[3],
                    C = 4,
                    P = 1; P < n; P++)
                        E = u[R >>> 24] ^ d[_ >> 16 & 255] ^ c[w >> 8 & 255] ^ h[255 & L] ^ o[C],
                        T = u[_ >>> 24] ^ d[w >> 16 & 255] ^ c[L >> 8 & 255] ^ h[255 & R] ^ o[C + 1],
                        S = u[w >>> 24] ^ d[L >> 16 & 255] ^ c[R >> 8 & 255] ^ h[255 & _] ^ o[C + 2],
                        A = u[L >>> 24] ^ d[R >> 16 & 255] ^ c[_ >> 8 & 255] ^ h[255 & w] ^ o[C + 3],
                        R = E,
                        _ = T,
                        w = S,
                        L = A,
                        C += 4;
                    E = s[R >>> 24] << 24 ^ s[_ >> 16 & 255] << 16 ^ s[w >> 8 & 255] << 8 ^ s[255 & L] ^ o[C],
                    T = s[_ >>> 24] << 24 ^ s[w >> 16 & 255] << 16 ^ s[L >> 8 & 255] << 8 ^ s[255 & R] ^ o[C + 1],
                    S = s[w >>> 24] << 24 ^ s[L >> 16 & 255] << 16 ^ s[R >> 8 & 255] << 8 ^ s[255 & _] ^ o[C + 2],
                    A = s[L >>> 24] << 24 ^ s[R >> 16 & 255] << 16 ^ s[_ >> 8 & 255] << 8 ^ s[255 & w] ^ o[C + 3],
                    C += 3,
                    b[e] = x(E ^ p),
                    b[e + 1] = x(A ^ g),
                    b[e + 2] = x(S ^ v),
                    b[e + 3] = x(T ^ y),
                    p = D,
                    g = I,
                    v = k,
                    y = O,
                    e += 4
                }
                return i ? a(b.buffer) : b.buffer
            }
            ,
            t.prototype.destroy = function() {
                this.key = void 0,
                this.keySize = void 0,
                this.ksRows = void 0,
                this.sBox = void 0,
                this.invSBox = void 0,
                this.subMix = void 0,
                this.invSubMix = void 0,
                this.keySchedule = void 0,
                this.invKeySchedule = void 0,
                this.rcon = void 0
            }
            ,
            t
        }();
        e.a = n
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(3)
          , n = r(23)
          , o = r(0)
          , s = r(9)
          , l = function() {
            function t(e, r, a) {
                i(this, t),
                this.observer = e,
                this.config = a,
                this.remuxer = r
            }
            return t.prototype.resetInitSegment = function(t, e, r, i) {
                this._audioTrack = {
                    container: "audio/adts",
                    type: "audio",
                    id: 0,
                    sequenceNumber: 0,
                    isAAC: !0,
                    samples: [],
                    len: 0,
                    manifestCodec: e,
                    duration: i,
                    inputTimeScale: 9e4
                }
            }
            ,
            t.prototype.resetTimeStamp = function() {}
            ,
            t.probe = function(t) {
                if (!t)
                    return !1;
                for (var e = s.a.getID3Data(t, 0) || [], r = e.length, i = t.length; r < i; r++)
                    if (n.e(t, r))
                        return o.b.log("ADTS sync word found !"),
                        !0;
                return !1
            }
            ,
            t.prototype.append = function(t, e, r, i) {
                for (var l = this._audioTrack, u = s.a.getID3Data(t, 0) || [], d = s.a.getTimeStamp(u), c = Object(a.a)(d) ? 90 * d : 9e4 * e, h = 0, f = c, p = t.length, g = u.length, v = [{
                    pts: f,
                    dts: f,
                    data: u
                }]; g < p - 1; )
                    if (n.d(t, g) && g + 5 < p) {
                        n.c(l, this.observer, t, g, l.manifestCodec);
                        var y = n.a(l, t, g, c, h);
                        if (!y) {
                            o.b.log("Unable to parse AAC frame");
                            break
                        }
                        g += y.length,
                        f = y.sample.pts,
                        h++
                    } else
                        s.a.isHeader(t, g) ? (u = s.a.getID3Data(t, g),
                        v.push({
                            pts: f,
                            dts: f,
                            data: u
                        }),
                        g += u.length) : g++;
                this.remuxer.remux(l, {
                    samples: []
                }, {
                    samples: v,
                    inputTimeScale: 9e4
                }, {
                    samples: []
                }, e, r, i)
            }
            ,
            t.prototype.destroy = function() {}
            ,
            t
        }();
        e.a = l
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(23)
          , n = r(24)
          , o = r(1)
          , s = r(42)
          , l = r(43)
          , u = r(0)
          , d = r(2)
          , c = {
            video: 1,
            audio: 2,
            id3: 3,
            text: 4
        }
          , h = function() {
            function t(e, r, a, n) {
                i(this, t),
                this.observer = e,
                this.config = a,
                this.typeSupported = n,
                this.remuxer = r,
                this.sampleAes = null
            }
            return t.prototype.setDecryptData = function(t) {
                null != t && null != t.key && "SAMPLE-AES" === t.method ? this.sampleAes = new l.a(this.observer,this.config,t,this.discardEPB) : this.sampleAes = null
            }
            ,
            t.probe = function(e) {
                var r = t._syncOffset(e);
                return !(r < 0) && (r && u.b.warn("MPEG2-TS detected but first sync word found @ offset " + r + ", junk ahead ?"),
                !0)
            }
            ,
            t._syncOffset = function(t) {
                for (var e = Math.min(1e3, t.length - 564), r = 0; r < e; ) {
                    if (71 === t[r] && 71 === t[r + 188] && 71 === t[r + 376])
                        return r;
                    r++
                }
                return -1
            }
            ,
            t.createTrack = function(t, e) {
                return {
                    container: "video" === t || "audio" === t ? "video/mp2t" : void 0,
                    type: t,
                    id: c[t],
                    pid: -1,
                    inputTimeScale: 9e4,
                    sequenceNumber: 0,
                    samples: [],
                    len: 0,
                    dropped: "video" === t ? 0 : void 0,
                    isAAC: "audio" === t || void 0,
                    duration: "audio" === t ? e : void 0
                }
            }
            ,
            t.prototype.resetInitSegment = function(e, r, i, a) {
                this.pmtParsed = !1,
                this._pmtId = -1,
                this._avcTrack = t.createTrack("video", a),
                this._audioTrack = t.createTrack("audio", a),
                this._id3Track = t.createTrack("id3", a),
                this._txtTrack = t.createTrack("text", a),
                this.aacOverFlow = null,
                this.aacLastPTS = null,
                this.avcSample = null,
                this.audioCodec = r,
                this.videoCodec = i,
                this._duration = a
            }
            ,
            t.prototype.resetTimeStamp = function() {}
            ,
            t.prototype.append = function(e, r, i, a) {
                var n = void 0
                  , s = e.length
                  , l = void 0
                  , c = void 0
                  , h = void 0
                  , f = void 0
                  , p = !1;
                this.contiguous = i;
                var g = this.pmtParsed
                  , v = this._avcTrack
                  , y = this._audioTrack
                  , m = this._id3Track
                  , b = v.pid
                  , E = y.pid
                  , T = m.pid
                  , S = this._pmtId
                  , A = v.pesData
                  , R = y.pesData
                  , _ = m.pesData
                  , w = this._parsePAT
                  , L = this._parsePMT
                  , D = this._parsePES
                  , I = this._parseAVCPES.bind(this)
                  , k = this._parseAACPES.bind(this)
                  , O = this._parseMPEGPES.bind(this)
                  , C = this._parseID3PES.bind(this)
                  , P = t._syncOffset(e);
                for (s -= (s + P) % 188,
                n = P; n < s; n += 188)
                    if (71 === e[n]) {
                        if (l = !!(64 & e[n + 1]),
                        c = ((31 & e[n + 1]) << 8) + e[n + 2],
                        (48 & e[n + 3]) >> 4 > 1) {
                            if ((h = n + 5 + e[n + 4]) === n + 188)
                                continue
                        } else
                            h = n + 4;
                        switch (c) {
                        case b:
                            l && (A && (f = D(A)) && void 0 !== f.pts && I(f, !1),
                            A = {
                                data: [],
                                size: 0
                            }),
                            A && (A.data.push(e.subarray(h, n + 188)),
                            A.size += n + 188 - h);
                            break;
                        case E:
                            l && (R && (f = D(R)) && void 0 !== f.pts && (y.isAAC ? k(f) : O(f)),
                            R = {
                                data: [],
                                size: 0
                            }),
                            R && (R.data.push(e.subarray(h, n + 188)),
                            R.size += n + 188 - h);
                            break;
                        case T:
                            l && (_ && (f = D(_)) && void 0 !== f.pts && C(f),
                            _ = {
                                data: [],
                                size: 0
                            }),
                            _ && (_.data.push(e.subarray(h, n + 188)),
                            _.size += n + 188 - h);
                            break;
                        case 0:
                            l && (h += e[h] + 1),
                            S = this._pmtId = w(e, h);
                            break;
                        case S:
                            l && (h += e[h] + 1);
                            var x = L(e, h, !0 === this.typeSupported.mpeg || !0 === this.typeSupported.mp3, null != this.sampleAes);
                            b = x.avc,
                            b > 0 && (v.pid = b),
                            E = x.audio,
                            E > 0 && (y.pid = E,
                            y.isAAC = x.isAAC),
                            T = x.id3,
                            T > 0 && (m.pid = T),
                            p && !g && (u.b.log("reparse from beginning"),
                            p = !1,
                            n = P - 188),
                            g = this.pmtParsed = !0;
                            break;
                        case 17:
                        case 8191:
                            break;
                        default:
                            p = !0
                        }
                    } else
                        this.observer.trigger(o.a.ERROR, {
                            type: d.b.MEDIA_ERROR,
                            details: d.a.FRAG_PARSING_ERROR,
                            fatal: !1,
                            reason: "TS packet did not start with 0x47"
                        });
                A && (f = D(A)) && void 0 !== f.pts ? (I(f, !0),
                v.pesData = null) : v.pesData = A,
                R && (f = D(R)) && void 0 !== f.pts ? (y.isAAC ? k(f) : O(f),
                y.pesData = null) : (R && R.size && u.b.log("last AAC PES packet truncated,might overlap between fragments"),
                y.pesData = R),
                _ && (f = D(_)) && void 0 !== f.pts ? (C(f),
                m.pesData = null) : m.pesData = _,
                null == this.sampleAes ? this.remuxer.remux(y, v, m, this._txtTrack, r, i, a) : this.decryptAndRemux(y, v, m, this._txtTrack, r, i, a)
            }
            ,
            t.prototype.decryptAndRemux = function(t, e, r, i, a, n, o) {
                if (t.samples && t.isAAC) {
                    var s = this;
                    this.sampleAes.decryptAacSamples(t.samples, 0, function() {
                        s.decryptAndRemuxAvc(t, e, r, i, a, n, o)
                    })
                } else
                    this.decryptAndRemuxAvc(t, e, r, i, a, n, o)
            }
            ,
            t.prototype.decryptAndRemuxAvc = function(t, e, r, i, a, n, o) {
                if (e.samples) {
                    var s = this;
                    this.sampleAes.decryptAvcSamples(e.samples, 0, 0, function() {
                        s.remuxer.remux(t, e, r, i, a, n, o)
                    })
                } else
                    this.remuxer.remux(t, e, r, i, a, n, o)
            }
            ,
            t.prototype.destroy = function() {
                this._initPTS = this._initDTS = void 0,
                this._duration = 0
            }
            ,
            t.prototype._parsePAT = function(t, e) {
                return (31 & t[e + 10]) << 8 | t[e + 11]
            }
            ,
            t.prototype._parsePMT = function(t, e, r, i) {
                var a = void 0
                  , n = void 0
                  , o = void 0
                  , s = void 0
                  , l = {
                    audio: -1,
                    avc: -1,
                    id3: -1,
                    isAAC: !0
                };
                for (a = (15 & t[e + 1]) << 8 | t[e + 2],
                n = e + 3 + a - 4,
                o = (15 & t[e + 10]) << 8 | t[e + 11],
                e += 12 + o; e < n; ) {
                    switch (s = (31 & t[e + 1]) << 8 | t[e + 2],
                    t[e]) {
                    case 207:
                        if (!i) {
                            u.b.log("unkown stream type:" + t[e]);
                            break
                        }
                    case 15:
                        -1 === l.audio && (l.audio = s);
                        break;
                    case 21:
                        -1 === l.id3 && (l.id3 = s);
                        break;
                    case 219:
                        if (!i) {
                            u.b.log("unkown stream type:" + t[e]);
                            break
                        }
                    case 27:
                        -1 === l.avc && (l.avc = s);
                        break;
                    case 3:
                    case 4:
                        r ? -1 === l.audio && (l.audio = s,
                        l.isAAC = !1) : u.b.log("MPEG audio found, not supported in this browser for now");
                        break;
                    case 36:
                        u.b.warn("HEVC stream type found, not supported for now");
                        break;
                    default:
                        u.b.log("unkown stream type:" + t[e])
                    }
                    e += 5 + ((15 & t[e + 3]) << 8 | t[e + 4])
                }
                return l
            }
            ,
            t.prototype._parsePES = function(t) {
                var e = 0
                  , r = void 0
                  , i = void 0
                  , a = void 0
                  , n = void 0
                  , o = void 0
                  , s = void 0
                  , l = void 0
                  , d = void 0
                  , c = t.data;
                if (!t || 0 === t.size)
                    return null;
                for (; c[0].length < 19 && c.length > 1; ) {
                    var h = new Uint8Array(c[0].length + c[1].length);
                    h.set(c[0]),
                    h.set(c[1], c[0].length),
                    c[0] = h,
                    c.splice(1, 1)
                }
                if (r = c[0],
                1 === (r[0] << 16) + (r[1] << 8) + r[2]) {
                    if ((a = (r[4] << 8) + r[5]) && a > t.size - 6)
                        return null;
                    i = r[7],
                    192 & i && (s = 536870912 * (14 & r[9]) + 4194304 * (255 & r[10]) + 16384 * (254 & r[11]) + 128 * (255 & r[12]) + (254 & r[13]) / 2,
                    s > 4294967295 && (s -= 8589934592),
                    64 & i ? (l = 536870912 * (14 & r[14]) + 4194304 * (255 & r[15]) + 16384 * (254 & r[16]) + 128 * (255 & r[17]) + (254 & r[18]) / 2,
                    l > 4294967295 && (l -= 8589934592),
                    s - l > 54e5 && (u.b.warn(Math.round((s - l) / 9e4) + "s delta between PTS and DTS, align them"),
                    s = l)) : l = s),
                    n = r[8],
                    d = n + 9,
                    t.size -= d,
                    o = new Uint8Array(t.size);
                    for (var f = 0, p = c.length; f < p; f++) {
                        r = c[f];
                        var g = r.byteLength;
                        if (d) {
                            if (d > g) {
                                d -= g;
                                continue
                            }
                            r = r.subarray(d),
                            g -= d,
                            d = 0
                        }
                        o.set(r, e),
                        e += g
                    }
                    return a && (a -= n + 3),
                    {
                        data: o,
                        pts: s,
                        dts: l,
                        len: a
                    }
                }
                return null
            }
            ,
            t.prototype.pushAccesUnit = function(t, e) {
                if (t.units.length && t.frame) {
                    var r = e.samples
                      , i = r.length;
                    !this.config.forceKeyFrameOnDiscontinuity || !0 === t.key || e.sps && (i || this.contiguous) ? (t.id = i,
                    r.push(t)) : e.dropped++
                }
                t.debug.length && u.b.log(t.pts + "/" + t.dts + ":" + t.debug)
            }
            ,
            t.prototype._parseAVCPES = function(t, e) {
                var r = this
                  , i = this._avcTrack
                  , a = this._parseAVCNALu(t.data)
                  , n = void 0
                  , o = this.avcSample
                  , l = void 0
                  , u = !1
                  , d = void 0
                  , c = this.pushAccesUnit.bind(this)
                  , h = function(t, e, r, i) {
                    return {
                        key: t,
                        pts: e,
                        dts: r,
                        units: [],
                        debug: i
                    }
                };
                t.data = null,
                o && a.length && !i.audFound && (c(o, i),
                o = this.avcSample = h(!1, t.pts, t.dts, "")),
                a.forEach(function(e) {
                    switch (e.type) {
                    case 1:
                        l = !0,
                        o || (o = r.avcSample = h(!0, t.pts, t.dts, "")),
                        o.frame = !0;
                        var a = e.data;
                        if (u && a.length > 4) {
                            var f = new s.a(a).readSliceType();
                            2 !== f && 4 !== f && 7 !== f && 9 !== f || (o.key = !0)
                        }
                        break;
                    case 5:
                        l = !0,
                        o || (o = r.avcSample = h(!0, t.pts, t.dts, "")),
                        o.key = !0,
                        o.frame = !0;
                        break;
                    case 6:
                        l = !0,
                        n = new s.a(r.discardEPB(e.data)),
                        n.readUByte();
                        for (var p = 0, g = 0, v = !1, y = 0; !v && n.bytesAvailable > 1; ) {
                            p = 0;
                            do {
                                y = n.readUByte(),
                                p += y
                            } while (255 === y);
                            g = 0;
                            do {
                                y = n.readUByte(),
                                g += y
                            } while (255 === y);
                            if (4 === p && 0 !== n.bytesAvailable) {
                                v = !0;
                                if (181 === n.readUByte()) {
                                    if (49 === n.readUShort()) {
                                        if (1195456820 === n.readUInt()) {
                                            if (3 === n.readUByte()) {
                                                var m = n.readUByte()
                                                  , b = n.readUByte()
                                                  , E = 31 & m
                                                  , T = [m, b];
                                                for (d = 0; d < E; d++)
                                                    T.push(n.readUByte()),
                                                    T.push(n.readUByte()),
                                                    T.push(n.readUByte());
                                                r._insertSampleInOrder(r._txtTrack.samples, {
                                                    type: 3,
                                                    pts: t.pts,
                                                    bytes: T
                                                })
                                            }
                                        }
                                    }
                                }
                            } else if (g < n.bytesAvailable)
                                for (d = 0; d < g; d++)
                                    n.readUByte()
                        }
                        break;
                    case 7:
                        if (l = !0,
                        u = !0,
                        !i.sps) {
                            n = new s.a(e.data);
                            var S = n.readSPS();
                            i.width = S.width,
                            i.height = S.height,
                            i.pixelRatio = S.pixelRatio,
                            i.sps = [e.data],
                            i.duration = r._duration;
                            var A = e.data.subarray(1, 4)
                              , R = "avc1.";
                            for (d = 0; d < 3; d++) {
                                var _ = A[d].toString(16);
                                _.length < 2 && (_ = "0" + _),
                                R += _
                            }
                            i.codec = R
                        }
                        break;
                    case 8:
                        l = !0,
                        i.pps || (i.pps = [e.data]);
                        break;
                    case 9:
                        l = !1,
                        i.audFound = !0,
                        o && c(o, i),
                        o = r.avcSample = h(!1, t.pts, t.dts, "");
                        break;
                    case 12:
                        l = !1;
                        break;
                    default:
                        l = !1,
                        o && (o.debug += "unknown NAL " + e.type + " ")
                    }
                    if (o && l) {
                        o.units.push(e)
                    }
                }),
                e && o && (c(o, i),
                this.avcSample = null)
            }
            ,
            t.prototype._insertSampleInOrder = function(t, e) {
                var r = t.length;
                if (r > 0) {
                    if (e.pts >= t[r - 1].pts)
                        t.push(e);
                    else
                        for (var i = r - 1; i >= 0; i--)
                            if (e.pts < t[i].pts) {
                                t.splice(i, 0, e);
                                break
                            }
                } else
                    t.push(e)
            }
            ,
            t.prototype._getLastNalUnit = function() {
                var t = this.avcSample
                  , e = void 0;
                if (!t || 0 === t.units.length) {
                    var r = this._avcTrack
                      , i = r.samples;
                    t = i[i.length - 1]
                }
                if (t) {
                    var a = t.units;
                    e = a[a.length - 1]
                }
                return e
            }
            ,
            t.prototype._parseAVCNALu = function(t) {
                var e = 0
                  , r = t.byteLength
                  , i = void 0
                  , a = void 0
                  , n = this._avcTrack
                  , o = n.naluState || 0
                  , s = o
                  , l = []
                  , u = void 0
                  , d = void 0
                  , c = -1
                  , h = void 0;
                for (-1 === o && (c = 0,
                h = 31 & t[0],
                o = 0,
                e = 1); e < r; )
                    if (i = t[e++],
                    o)
                        if (1 !== o)
                            if (i)
                                if (1 === i) {
                                    if (c >= 0)
                                        u = {
                                            data: t.subarray(c, e - o - 1),
                                            type: h
                                        },
                                        l.push(u);
                                    else {
                                        var f = this._getLastNalUnit();
                                        if (f && (s && e <= 4 - s && f.state && (f.data = f.data.subarray(0, f.data.byteLength - s)),
                                        (a = e - o - 1) > 0)) {
                                            var p = new Uint8Array(f.data.byteLength + a);
                                            p.set(f.data, 0),
                                            p.set(t.subarray(0, a), f.data.byteLength),
                                            f.data = p
                                        }
                                    }
                                    e < r ? (d = 31 & t[e],
                                    c = e,
                                    h = d,
                                    o = 0) : o = -1
                                } else
                                    o = 0;
                            else
                                o = 3;
                        else
                            o = i ? 0 : 2;
                    else
                        o = i ? 0 : 1;
                if (c >= 0 && o >= 0 && (u = {
                    data: t.subarray(c, r),
                    type: h,
                    state: o
                },
                l.push(u)),
                0 === l.length) {
                    var g = this._getLastNalUnit();
                    if (g) {
                        var v = new Uint8Array(g.data.byteLength + t.byteLength);
                        v.set(g.data, 0),
                        v.set(t, g.data.byteLength),
                        g.data = v
                    }
                }
                return n.naluState = o,
                l
            }
            ,
            t.prototype.discardEPB = function(t) {
                for (var e = t.byteLength, r = [], i = 1, a = void 0, n = void 0; i < e - 2; )
                    0 === t[i] && 0 === t[i + 1] && 3 === t[i + 2] ? (r.push(i + 2),
                    i += 2) : i++;
                if (0 === r.length)
                    return t;
                a = e - r.length,
                n = new Uint8Array(a);
                var o = 0;
                for (i = 0; i < a; o++,
                i++)
                    o === r[0] && (o++,
                    r.shift()),
                    n[i] = t[o];
                return n
            }
            ,
            t.prototype._parseAACPES = function(t) {
                var e = this._audioTrack
                  , r = t.data
                  , i = t.pts
                  , n = this.aacOverFlow
                  , s = this.aacLastPTS
                  , l = void 0
                  , c = void 0
                  , h = void 0
                  , f = void 0
                  , p = void 0;
                if (n) {
                    var g = new Uint8Array(n.byteLength + r.byteLength);
                    g.set(n, 0),
                    g.set(r, n.byteLength),
                    r = g
                }
                for (h = 0,
                p = r.length; h < p - 1 && !a.d(r, h); h++)
                    ;
                if (h) {
                    var v = void 0
                      , y = void 0;
                    if (h < p - 1 ? (v = "AAC PES did not start with ADTS header,offset:" + h,
                    y = !1) : (v = "no ADTS header found in AAC PES",
                    y = !0),
                    u.b.warn("parsing error:" + v),
                    this.observer.trigger(o.a.ERROR, {
                        type: d.b.MEDIA_ERROR,
                        details: d.a.FRAG_PARSING_ERROR,
                        fatal: y,
                        reason: v
                    }),
                    y)
                        return
                }
                if (a.c(e, this.observer, r, h, this.audioCodec),
                c = 0,
                l = a.b(e.samplerate),
                n && s) {
                    var m = s + l;
                    Math.abs(m - i) > 1 && (u.b.log("AAC: align PTS for overlapping frames by " + Math.round((m - i) / 90)),
                    i = m)
                }
                for (; h < p; )
                    if (a.d(r, h) && h + 5 < p) {
                        var b = a.a(e, r, h, i, c);
                        if (!b)
                            break;
                        h += b.length,
                        f = b.sample.pts,
                        c++
                    } else
                        h++;
                n = h < p ? r.subarray(h, p) : null,
                this.aacOverFlow = n,
                this.aacLastPTS = f
            }
            ,
            t.prototype._parseMPEGPES = function(t) {
                for (var e = t.data, r = e.length, i = 0, a = 0, o = t.pts; a < r; )
                    if (n.a.isHeader(e, a)) {
                        var s = n.a.appendFrame(this._audioTrack, e, a, o, i);
                        if (!s)
                            break;
                        a += s.length,
                        i++
                    } else
                        a++
            }
            ,
            t.prototype._parseID3PES = function(t) {
                this._id3Track.samples.push(t)
            }
            ,
            t
        }();
        e.a = h
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(0)
          , n = function() {
            function t(e) {
                i(this, t),
                this.data = e,
                this.bytesAvailable = e.byteLength,
                this.word = 0,
                this.bitsAvailable = 0
            }
            return t.prototype.loadWord = function() {
                var t = this.data
                  , e = this.bytesAvailable
                  , r = t.byteLength - e
                  , i = new Uint8Array(4)
                  , a = Math.min(4, e);
                if (0 === a)
                    throw new Error("no bytes available");
                i.set(t.subarray(r, r + a)),
                this.word = new DataView(i.buffer).getUint32(0),
                this.bitsAvailable = 8 * a,
                this.bytesAvailable -= a
            }
            ,
            t.prototype.skipBits = function(t) {
                var e = void 0;
                this.bitsAvailable > t ? (this.word <<= t,
                this.bitsAvailable -= t) : (t -= this.bitsAvailable,
                e = t >> 3,
                t -= e >> 3,
                this.bytesAvailable -= e,
                this.loadWord(),
                this.word <<= t,
                this.bitsAvailable -= t)
            }
            ,
            t.prototype.readBits = function(t) {
                var e = Math.min(this.bitsAvailable, t)
                  , r = this.word >>> 32 - e;
                return t > 32 && a.b.error("Cannot read more than 32 bits at a time"),
                this.bitsAvailable -= e,
                this.bitsAvailable > 0 ? this.word <<= e : this.bytesAvailable > 0 && this.loadWord(),
                e = t - e,
                e > 0 && this.bitsAvailable ? r << e | this.readBits(e) : r
            }
            ,
            t.prototype.skipLZ = function() {
                var t = void 0;
                for (t = 0; t < this.bitsAvailable; ++t)
                    if (0 != (this.word & 2147483648 >>> t))
                        return this.word <<= t,
                        this.bitsAvailable -= t,
                        t;
                return this.loadWord(),
                t + this.skipLZ()
            }
            ,
            t.prototype.skipUEG = function() {
                this.skipBits(1 + this.skipLZ())
            }
            ,
            t.prototype.skipEG = function() {
                this.skipBits(1 + this.skipLZ())
            }
            ,
            t.prototype.readUEG = function() {
                var t = this.skipLZ();
                return this.readBits(t + 1) - 1
            }
            ,
            t.prototype.readEG = function() {
                var t = this.readUEG();
                return 1 & t ? 1 + t >>> 1 : -1 * (t >>> 1)
            }
            ,
            t.prototype.readBoolean = function() {
                return 1 === this.readBits(1)
            }
            ,
            t.prototype.readUByte = function() {
                return this.readBits(8)
            }
            ,
            t.prototype.readUShort = function() {
                return this.readBits(16)
            }
            ,
            t.prototype.readUInt = function() {
                return this.readBits(32)
            }
            ,
            t.prototype.skipScalingList = function(t) {
                var e = 8
                  , r = 8
                  , i = void 0
                  , a = void 0;
                for (i = 0; i < t; i++)
                    0 !== r && (a = this.readEG(),
                    r = (e + a + 256) % 256),
                    e = 0 === r ? e : r
            }
            ,
            t.prototype.readSPS = function() {
                var t = 0
                  , e = 0
                  , r = 0
                  , i = 0
                  , a = void 0
                  , n = void 0
                  , o = void 0
                  , s = void 0
                  , l = void 0
                  , u = void 0
                  , d = void 0
                  , c = this.readUByte.bind(this)
                  , h = this.readBits.bind(this)
                  , f = this.readUEG.bind(this)
                  , p = this.readBoolean.bind(this)
                  , g = this.skipBits.bind(this)
                  , v = this.skipEG.bind(this)
                  , y = this.skipUEG.bind(this)
                  , m = this.skipScalingList.bind(this);
                if (c(),
                a = c(),
                h(5),
                g(3),
                c(),
                y(),
                100 === a || 110 === a || 122 === a || 244 === a || 44 === a || 83 === a || 86 === a || 118 === a || 128 === a) {
                    var b = f();
                    if (3 === b && g(1),
                    y(),
                    y(),
                    g(1),
                    p())
                        for (u = 3 !== b ? 8 : 12,
                        d = 0; d < u; d++)
                            p() && m(d < 6 ? 16 : 64)
                }
                y();
                var E = f();
                if (0 === E)
                    f();
                else if (1 === E)
                    for (g(1),
                    v(),
                    v(),
                    n = f(),
                    d = 0; d < n; d++)
                        v();
                y(),
                g(1),
                o = f(),
                s = f(),
                l = h(1),
                0 === l && g(1),
                g(1),
                p() && (t = f(),
                e = f(),
                r = f(),
                i = f());
                var T = [1, 1];
                if (p() && p()) {
                    switch (c()) {
                    case 1:
                        T = [1, 1];
                        break;
                    case 2:
                        T = [12, 11];
                        break;
                    case 3:
                        T = [10, 11];
                        break;
                    case 4:
                        T = [16, 11];
                        break;
                    case 5:
                        T = [40, 33];
                        break;
                    case 6:
                        T = [24, 11];
                        break;
                    case 7:
                        T = [20, 11];
                        break;
                    case 8:
                        T = [32, 11];
                        break;
                    case 9:
                        T = [80, 33];
                        break;
                    case 10:
                        T = [18, 11];
                        break;
                    case 11:
                        T = [15, 11];
                        break;
                    case 12:
                        T = [64, 33];
                        break;
                    case 13:
                        T = [160, 99];
                        break;
                    case 14:
                        T = [4, 3];
                        break;
                    case 15:
                        T = [3, 2];
                        break;
                    case 16:
                        T = [2, 1];
                        break;
                    case 255:
                        T = [c() << 8 | c(), c() << 8 | c()]
                    }
                }
                return {
                    width: Math.ceil(16 * (o + 1) - 2 * t - 2 * e),
                    height: (2 - l) * (s + 1) * 16 - (l ? 2 : 4) * (r + i),
                    pixelRatio: T
                }
            }
            ,
            t.prototype.readSliceType = function() {
                return this.readUByte(),
                this.readUEG(),
                this.readUEG()
            }
            ,
            t
        }();
        e.a = n
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(14)
          , n = function() {
            function t(e, r, n, o) {
                i(this, t),
                this.decryptdata = n,
                this.discardEPB = o,
                this.decrypter = new a.a(e,r,{
                    removePKCS7Padding: !1
                })
            }
            return t.prototype.decryptBuffer = function(t, e) {
                this.decrypter.decrypt(t, this.decryptdata.key.buffer, this.decryptdata.iv.buffer, e)
            }
            ,
            t.prototype.decryptAacSample = function(t, e, r, i) {
                var a = t[e].unit
                  , n = a.subarray(16, a.length - a.length % 16)
                  , o = n.buffer.slice(n.byteOffset, n.byteOffset + n.length)
                  , s = this;
                this.decryptBuffer(o, function(n) {
                    n = new Uint8Array(n),
                    a.set(n, 16),
                    i || s.decryptAacSamples(t, e + 1, r)
                })
            }
            ,
            t.prototype.decryptAacSamples = function(t, e, r) {
                for (; ; e++) {
                    if (e >= t.length)
                        return void r();
                    if (!(t[e].unit.length < 32)) {
                        var i = this.decrypter.isSync();
                        if (this.decryptAacSample(t, e, r, i),
                        !i)
                            return
                    }
                }
            }
            ,
            t.prototype.getAvcEncryptedData = function(t) {
                for (var e = 16 * Math.floor((t.length - 48) / 160) + 16, r = new Int8Array(e), i = 0, a = 32; a <= t.length - 16; a += 160,
                i += 16)
                    r.set(t.subarray(a, a + 16), i);
                return r
            }
            ,
            t.prototype.getAvcDecryptedUnit = function(t, e) {
                e = new Uint8Array(e);
                for (var r = 0, i = 32; i <= t.length - 16; i += 160,
                r += 16)
                    t.set(e.subarray(r, r + 16), i);
                return t
            }
            ,
            t.prototype.decryptAvcSample = function(t, e, r, i, a, n) {
                var o = this.discardEPB(a.data)
                  , s = this.getAvcEncryptedData(o)
                  , l = this;
                this.decryptBuffer(s.buffer, function(s) {
                    a.data = l.getAvcDecryptedUnit(o, s),
                    n || l.decryptAvcSamples(t, e, r + 1, i)
                })
            }
            ,
            t.prototype.decryptAvcSamples = function(t, e, r, i) {
                for (; ; e++,
                r = 0) {
                    if (e >= t.length)
                        return void i();
                    for (var a = t[e].units; !(r >= a.length); r++) {
                        var n = a[r];
                        if (!(n.length <= 48 || 1 !== n.type && 5 !== n.type)) {
                            var o = this.decrypter.isSync();
                            if (this.decryptAvcSample(t, e, r, i, n, o),
                            !o)
                                return
                        }
                    }
                }
            }
            ,
            t
        }();
        e.a = n
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(9)
          , n = r(0)
          , o = r(24)
          , s = function() {
            function t(e, r, a) {
                i(this, t),
                this.observer = e,
                this.config = a,
                this.remuxer = r
            }
            return t.prototype.resetInitSegment = function(t, e, r, i) {
                this._audioTrack = {
                    container: "audio/mpeg",
                    type: "audio",
                    id: -1,
                    sequenceNumber: 0,
                    isAAC: !1,
                    samples: [],
                    len: 0,
                    manifestCodec: e,
                    duration: i,
                    inputTimeScale: 9e4
                }
            }
            ,
            t.prototype.resetTimeStamp = function() {}
            ,
            t.probe = function(t) {
                var e = void 0
                  , r = void 0
                  , i = a.a.getID3Data(t, 0);
                if (i && void 0 !== a.a.getTimeStamp(i))
                    for (e = i.length,
                    r = Math.min(t.length - 1, e + 100); e < r; e++)
                        if (o.a.probe(t, e))
                            return n.b.log("MPEG Audio sync word found !"),
                            !0;
                return !1
            }
            ,
            t.prototype.append = function(t, e, r, i) {
                for (var n = a.a.getID3Data(t, 0), s = a.a.getTimeStamp(n), l = s ? 90 * s : 9e4 * e, u = n.length, d = t.length, c = 0, h = 0, f = this._audioTrack, p = [{
                    pts: l,
                    dts: l,
                    data: n
                }]; u < d; )
                    if (o.a.isHeader(t, u)) {
                        var g = o.a.appendFrame(f, t, u, l, c);
                        if (!g)
                            break;
                        u += g.length,
                        h = g.sample.pts,
                        c++
                    } else
                        a.a.isHeader(t, u) ? (n = a.a.getID3Data(t, u),
                        p.push({
                            pts: h,
                            dts: h,
                            data: n
                        }),
                        u += n.length) : u++;
                this.remuxer.remux(f, {
                    samples: []
                }, {
                    samples: p,
                    inputTimeScale: 9e4
                }, {
                    samples: []
                }, e, r, i)
            }
            ,
            t.prototype.destroy = function() {}
            ,
            t
        }();
        e.a = s
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(46)
          , n = r(47)
          , o = r(1)
          , s = r(2)
          , l = r(0)
          , u = function() {
            function t(e, r, a, n) {
                i(this, t),
                this.observer = e,
                this.config = r,
                this.typeSupported = a;
                var o = navigator.userAgent;
                this.isSafari = n && n.indexOf("Apple") > -1 && o && !o.match("CriOS"),
                this.ISGenerated = !1
            }
            return t.prototype.destroy = function() {}
            ,
            t.prototype.resetTimeStamp = function(t) {
                this._initPTS = this._initDTS = t
            }
            ,
            t.prototype.resetInitSegment = function() {
                this.ISGenerated = !1
            }
            ,
            t.prototype.remux = function(t, e, r, i, a, n, s) {
                if (this.ISGenerated || this.generateIS(t, e, a),
                this.ISGenerated) {
                    var u = t.samples.length
                      , d = e.samples.length
                      , c = a
                      , h = a;
                    if (u && d) {
                        var f = (t.samples[0].dts - e.samples[0].dts) / e.inputTimeScale;
                        c += Math.max(0, f),
                        h += Math.max(0, -f)
                    }
                    if (u) {
                        t.timescale || (l.b.warn("regenerate InitSegment as audio detected"),
                        this.generateIS(t, e, a));
                        var p = this.remuxAudio(t, c, n, s);
                        if (d) {
                            var g = void 0;
                            p && (g = p.endPTS - p.startPTS),
                            e.timescale || (l.b.warn("regenerate InitSegment as video detected"),
                            this.generateIS(t, e, a)),
                            this.remuxVideo(e, h, n, g, s)
                        }
                    } else if (d) {
                        var v = this.remuxVideo(e, h, n, 0, s);
                        v && t.codec && this.remuxEmptyAudio(t, c, n, v)
                    }
                }
                r.samples.length && this.remuxID3(r, a),
                i.samples.length && this.remuxText(i, a),
                this.observer.trigger(o.a.FRAG_PARSED)
            }
            ,
            t.prototype.generateIS = function(t, e, r) {
                var i = this.observer
                  , a = t.samples
                  , u = e.samples
                  , d = this.typeSupported
                  , c = "audio/mp4"
                  , h = {}
                  , f = {
                    tracks: h
                }
                  , p = void 0 === this._initPTS
                  , g = void 0
                  , v = void 0;
                if (p && (g = v = 1 / 0),
                t.config && a.length && (t.timescale = t.samplerate,
                l.b.log("audio sampling rate : " + t.samplerate),
                t.isAAC || (d.mpeg ? (c = "audio/mpeg",
                t.codec = "") : d.mp3 && (t.codec = "mp3")),
                h.audio = {
                    container: c,
                    codec: t.codec,
                    initSegment: !t.isAAC && d.mpeg ? new Uint8Array : n.a.initSegment([t]),
                    metadata: {
                        channelCount: t.channelCount
                    }
                },
                p && (g = v = a[0].pts - t.inputTimeScale * r)),
                e.sps && e.pps && u.length) {
                    var y = e.inputTimeScale;
                    e.timescale = y,
                    h.video = {
                        container: "video/mp4",
                        codec: e.codec,
                        initSegment: n.a.initSegment([e]),
                        metadata: {
                            width: e.width,
                            height: e.height
                        }
                    },
                    p && (g = Math.min(g, u[0].pts - y * r),
                    v = Math.min(v, u[0].dts - y * r),
                    this.observer.trigger(o.a.INIT_PTS_FOUND, {
                        initPTS: g
                    }))
                }
                Object.keys(h).length ? (i.trigger(o.a.FRAG_PARSING_INIT_SEGMENT, f),
                this.ISGenerated = !0,
                p && (this._initPTS = g,
                this._initDTS = v)) : i.trigger(o.a.ERROR, {
                    type: s.b.MEDIA_ERROR,
                    details: s.a.FRAG_PARSING_ERROR,
                    fatal: !1,
                    reason: "no audio/video samples found"
                })
            }
            ,
            t.prototype.remuxVideo = function(t, e, r, i, a) {
                var u = 8
                  , d = t.timescale
                  , c = void 0
                  , h = void 0
                  , f = void 0
                  , p = void 0
                  , g = void 0
                  , v = void 0
                  , y = void 0
                  , m = t.samples
                  , b = []
                  , E = m.length
                  , T = this._PTSNormalize
                  , S = this._initDTS
                  , A = this.nextAvcDts
                  , R = this.isSafari;
                if (0 !== E) {
                    R && (r |= m.length && A && (a && Math.abs(e - A / d) < .1 || Math.abs(m[0].pts - A - S) < d / 5)),
                    r || (A = e * d),
                    m.forEach(function(t) {
                        t.pts = T(t.pts - S, A),
                        t.dts = T(t.dts - S, A)
                    }),
                    m.sort(function(t, e) {
                        var r = t.dts - e.dts
                          , i = t.pts - e.pts;
                        return r || i || t.id - e.id
                    });
                    var _ = m.reduce(function(t, e) {
                        return Math.max(Math.min(t, e.pts - e.dts), -18e3)
                    }, 0);
                    if (_ < 0) {
                        l.b.warn("PTS < DTS detected in video samples, shifting DTS by " + Math.round(_ / 90) + " ms to overcome this issue");
                        for (var w = 0; w < m.length; w++)
                            m[w].dts += _
                    }
                    var L = m[0];
                    g = Math.max(L.dts, 0),
                    p = Math.max(L.pts, 0);
                    var D = Math.round((g - A) / 90);
                    r && D && (D > 1 ? l.b.log("AVC:" + D + " ms hole between fragments detected,filling it") : D < -1 && l.b.log("AVC:" + -D + " ms overlapping between fragments detected"),
                    g = A,
                    m[0].dts = g,
                    p = Math.max(p - D, A),
                    m[0].pts = p,
                    l.b.log("Video/PTS/DTS adjusted: " + Math.round(p / 90) + "/" + Math.round(g / 90) + ",delta:" + D + " ms")),
                    g,
                    L = m[m.length - 1],
                    y = Math.max(L.dts, 0),
                    v = Math.max(L.pts, 0, y),
                    R && (c = Math.round((y - g) / (m.length - 1)));
                    for (var I = 0, k = 0, O = 0; O < E; O++) {
                        for (var C = m[O], P = C.units, x = P.length, F = 0, M = 0; M < x; M++)
                            F += P[M].data.length;
                        k += F,
                        I += x,
                        C.length = F,
                        C.dts = R ? g + O * c : Math.max(C.dts, g),
                        C.pts = Math.max(C.pts, C.dts)
                    }
                    var N = k + 4 * I + 8;
                    try {
                        h = new Uint8Array(N)
                    } catch (t) {
                        return void this.observer.trigger(o.a.ERROR, {
                            type: s.b.MUX_ERROR,
                            details: s.a.REMUX_ALLOC_ERROR,
                            fatal: !1,
                            bytes: N,
                            reason: "fail allocating video mdat " + N
                        })
                    }
                    var U = new DataView(h.buffer);
                    U.setUint32(0, N),
                    h.set(n.a.types.mdat, 4);
                    for (var B = 0; B < E; B++) {
                        for (var G = m[B], K = G.units, j = 0, H = void 0, V = 0, Y = K.length; V < Y; V++) {
                            var W = K[V]
                              , q = W.data
                              , X = W.data.byteLength;
                            U.setUint32(u, X),
                            u += 4,
                            h.set(q, u),
                            u += X,
                            j += 4 + X
                        }
                        if (R)
                            H = Math.max(0, c * Math.round((G.pts - G.dts) / c));
                        else {
                            if (B < E - 1)
                                c = m[B + 1].dts - G.dts;
                            else {
                                var z = this.config
                                  , Q = G.dts - m[B > 0 ? B - 1 : B].dts;
                                if (z.stretchShortVideoTrack) {
                                    var $ = z.maxBufferHole
                                      , J = Math.floor($ * d)
                                      , Z = (i ? p + i * d : this.nextAudioPts) - G.pts;
                                    Z > J ? (c = Z - Q,
                                    c < 0 && (c = Q),
                                    l.b.log("It is approximately " + Z / 90 + " ms to the next segment; using duration " + c / 90 + " ms for the last video frame.")) : c = Q
                                } else
                                    c = Q
                            }
                            H = Math.round(G.pts - G.dts)
                        }
                        b.push({
                            size: j,
                            duration: c,
                            cts: H,
                            flags: {
                                isLeading: 0,
                                isDependedOn: 0,
                                hasRedundancy: 0,
                                degradPrio: 0,
                                dependsOn: G.key ? 2 : 1,
                                isNonSync: G.key ? 0 : 1
                            }
                        })
                    }
                    this.nextAvcDts = y + c;
                    var tt = t.dropped;
                    if (t.len = 0,
                    t.nbNalu = 0,
                    t.dropped = 0,
                    b.length && navigator.userAgent.toLowerCase().indexOf("chrome") > -1) {
                        var et = b[0].flags;
                        et.dependsOn = 2,
                        et.isNonSync = 0
                    }
                    t.samples = b,
                    f = n.a.moof(t.sequenceNumber++, g, t),
                    t.samples = [];
                    var rt = {
                        data1: f,
                        data2: h,
                        startPTS: p / d,
                        endPTS: (v + c) / d,
                        startDTS: g / d,
                        endDTS: this.nextAvcDts / d,
                        type: "video",
                        hasAudio: !1,
                        hasVideo: !0,
                        nb: b.length,
                        dropped: tt
                    };
                    return this.observer.trigger(o.a.FRAG_PARSING_DATA, rt),
                    rt
                }
            }
            ,
            t.prototype.remuxAudio = function(t, e, r, i) {
                var u = t.inputTimeScale
                  , d = t.timescale
                  , c = u / d
                  , h = t.isAAC ? 1024 : 1152
                  , f = h * c
                  , p = this._PTSNormalize
                  , g = this._initDTS
                  , v = !t.isAAC && this.typeSupported.mpeg
                  , y = void 0
                  , m = void 0
                  , b = void 0
                  , E = void 0
                  , T = void 0
                  , S = void 0
                  , A = void 0
                  , R = t.samples
                  , _ = []
                  , w = this.nextAudioPts;
                if (r |= R.length && w && (i && Math.abs(e - w / u) < .1 || Math.abs(R[0].pts - w - g) < 20 * f),
                R.forEach(function(t) {
                    t.pts = t.dts = p(t.pts - g, e * u)
                }),
                R = R.filter(function(t) {
                    return t.pts >= 0
                }),
                0 !== R.length) {
                    if (r || (w = i ? e * u : R[0].pts),
                    t.isAAC)
                        for (var L = this.config.maxAudioFramesDrift, D = 0, I = w; D < R.length; ) {
                            var k, O = R[D], C = O.pts;
                            k = C - I;
                            var P = Math.abs(1e3 * k / u);
                            if (k <= -L * f)
                                l.b.warn("Dropping 1 audio frame @ " + (I / u).toFixed(3) + "s due to " + Math.round(P) + " ms overlap."),
                                R.splice(D, 1),
                                t.len -= O.unit.length;
                            else if (k >= L * f && P < 1e4 && I) {
                                var x = Math.round(k / f);
                                l.b.warn("Injecting " + x + " audio frame @ " + (I / u).toFixed(3) + "s due to " + Math.round(1e3 * k / u) + " ms gap.");
                                for (var F = 0; F < x; F++) {
                                    var M = Math.max(I, 0);
                                    b = a.a.getSilentFrame(t.manifestCodec || t.codec, t.channelCount),
                                    b || (l.b.log("Unable to get silent frame for given audio codec; duplicating last frame instead."),
                                    b = O.unit.subarray()),
                                    R.splice(D, 0, {
                                        unit: b,
                                        pts: M,
                                        dts: M
                                    }),
                                    t.len += b.length,
                                    I += f,
                                    D++
                                }
                                O.pts = O.dts = I,
                                I += f,
                                D++
                            } else
                                Math.abs(k),
                                O.pts = O.dts = I,
                                I += f,
                                D++
                        }
                    for (var N = 0, U = R.length; N < U; N++) {
                        var B = R[N]
                          , G = B.unit
                          , K = B.pts;
                        if (void 0 !== A)
                            m.duration = Math.round((K - A) / c);
                        else {
                            var j = Math.round(1e3 * (K - w) / u)
                              , H = 0;
                            if (r && t.isAAC && j) {
                                if (j > 0 && j < 1e4)
                                    H = Math.round((K - w) / f),
                                    l.b.log(j + " ms hole between AAC samples detected,filling it"),
                                    H > 0 && (b = a.a.getSilentFrame(t.manifestCodec || t.codec, t.channelCount),
                                    b || (b = G.subarray()),
                                    t.len += H * b.length);
                                else if (j < -12) {
                                    l.b.log("drop overlapping AAC sample, expected/parsed/delta:" + (w / u).toFixed(3) + "s/" + (K / u).toFixed(3) + "s/" + -j + "ms"),
                                    t.len -= G.byteLength;
                                    continue
                                }
                                K = w
                            }
                            if (S = K,
                            !(t.len > 0))
                                return;
                            var V = v ? t.len : t.len + 8;
                            y = v ? 0 : 8;
                            try {
                                E = new Uint8Array(V)
                            } catch (t) {
                                return void this.observer.trigger(o.a.ERROR, {
                                    type: s.b.MUX_ERROR,
                                    details: s.a.REMUX_ALLOC_ERROR,
                                    fatal: !1,
                                    bytes: V,
                                    reason: "fail allocating audio mdat " + V
                                })
                            }
                            if (!v) {
                                new DataView(E.buffer).setUint32(0, V),
                                E.set(n.a.types.mdat, 4)
                            }
                            for (var Y = 0; Y < H; Y++)
                                b = a.a.getSilentFrame(t.manifestCodec || t.codec, t.channelCount),
                                b || (l.b.log("Unable to get silent frame for given audio codec; duplicating this frame instead."),
                                b = G.subarray()),
                                E.set(b, y),
                                y += b.byteLength,
                                m = {
                                    size: b.byteLength,
                                    cts: 0,
                                    duration: 1024,
                                    flags: {
                                        isLeading: 0,
                                        isDependedOn: 0,
                                        hasRedundancy: 0,
                                        degradPrio: 0,
                                        dependsOn: 1
                                    }
                                },
                                _.push(m)
                        }
                        E.set(G, y);
                        var W = G.byteLength;
                        y += W,
                        m = {
                            size: W,
                            cts: 0,
                            duration: 0,
                            flags: {
                                isLeading: 0,
                                isDependedOn: 0,
                                hasRedundancy: 0,
                                degradPrio: 0,
                                dependsOn: 1
                            }
                        },
                        _.push(m),
                        A = K
                    }
                    var q = 0
                      , X = _.length;
                    if (X >= 2 && (q = _[X - 2].duration,
                    m.duration = q),
                    X) {
                        this.nextAudioPts = w = A + c * q,
                        t.len = 0,
                        t.samples = _,
                        T = v ? new Uint8Array : n.a.moof(t.sequenceNumber++, S / c, t),
                        t.samples = [];
                        var z = S / u
                          , Q = w / u
                          , $ = {
                            data1: T,
                            data2: E,
                            startPTS: z,
                            endPTS: Q,
                            startDTS: z,
                            endDTS: Q,
                            type: "audio",
                            hasAudio: !0,
                            hasVideo: !1,
                            nb: X
                        };
                        return this.observer.trigger(o.a.FRAG_PARSING_DATA, $),
                        $
                    }
                    return null
                }
            }
            ,
            t.prototype.remuxEmptyAudio = function(t, e, r, i) {
                var n = t.inputTimeScale
                  , o = t.samplerate ? t.samplerate : n
                  , s = n / o
                  , u = this.nextAudioPts
                  , d = (void 0 !== u ? u : i.startDTS * n) + this._initDTS
                  , c = i.endDTS * n + this._initDTS
                  , h = 1024 * s
                  , f = Math.ceil((c - d) / h)
                  , p = a.a.getSilentFrame(t.manifestCodec || t.codec, t.channelCount);
                if (l.b.warn("remux empty Audio"),
                !p)
                    return void l.b.trace("Unable to remuxEmptyAudio since we were unable to get a silent frame for given audio codec!");
                for (var g = [], v = 0; v < f; v++) {
                    var y = d + v * h;
                    g.push({
                        unit: p,
                        pts: y,
                        dts: y
                    }),
                    t.len += p.length
                }
                t.samples = g,
                this.remuxAudio(t, e, r)
            }
            ,
            t.prototype.remuxID3 = function(t, e) {
                var r = t.samples.length
                  , i = void 0
                  , a = t.inputTimeScale
                  , n = this._initPTS
                  , s = this._initDTS;
                if (r) {
                    for (var l = 0; l < r; l++)
                        i = t.samples[l],
                        i.pts = (i.pts - n) / a,
                        i.dts = (i.dts - s) / a;
                    this.observer.trigger(o.a.FRAG_PARSING_METADATA, {
                        samples: t.samples
                    })
                }
                t.samples = [],
                e = e
            }
            ,
            t.prototype.remuxText = function(t, e) {
                t.samples.sort(function(t, e) {
                    return t.pts - e.pts
                });
                var r = t.samples.length
                  , i = void 0
                  , a = t.inputTimeScale
                  , n = this._initPTS;
                if (r) {
                    for (var s = 0; s < r; s++)
                        i = t.samples[s],
                        i.pts = (i.pts - n) / a;
                    this.observer.trigger(o.a.FRAG_PARSING_USERDATA, {
                        samples: t.samples
                    })
                }
                t.samples = [],
                e = e
            }
            ,
            t.prototype._PTSNormalize = function(t, e) {
                var r = void 0;
                if (void 0 === e)
                    return t;
                for (r = e < t ? -8589934592 : 8589934592; Math.abs(t - e) > 4294967296; )
                    t += r;
                return t
            }
            ,
            t
        }();
        e.a = u
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = function() {
            function t() {
                i(this, t)
            }
            return t.getSilentFrame = function(t, e) {
                switch (t) {
                case "mp4a.40.2":
                    if (1 === e)
                        return new Uint8Array([0, 200, 0, 128, 35, 128]);
                    if (2 === e)
                        return new Uint8Array([33, 0, 73, 144, 2, 25, 0, 35, 128]);
                    if (3 === e)
                        return new Uint8Array([0, 200, 0, 128, 32, 132, 1, 38, 64, 8, 100, 0, 142]);
                    if (4 === e)
                        return new Uint8Array([0, 200, 0, 128, 32, 132, 1, 38, 64, 8, 100, 0, 128, 44, 128, 8, 2, 56]);
                    if (5 === e)
                        return new Uint8Array([0, 200, 0, 128, 32, 132, 1, 38, 64, 8, 100, 0, 130, 48, 4, 153, 0, 33, 144, 2, 56]);
                    if (6 === e)
                        return new Uint8Array([0, 200, 0, 128, 32, 132, 1, 38, 64, 8, 100, 0, 130, 48, 4, 153, 0, 33, 144, 2, 0, 178, 0, 32, 8, 224]);
                    break;
                default:
                    if (1 === e)
                        return new Uint8Array([1, 64, 34, 128, 163, 78, 230, 128, 186, 8, 0, 0, 0, 28, 6, 241, 193, 10, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 94]);
                    if (2 === e)
                        return new Uint8Array([1, 64, 34, 128, 163, 94, 230, 128, 186, 8, 0, 0, 0, 0, 149, 0, 6, 241, 161, 10, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 94]);
                    if (3 === e)
                        return new Uint8Array([1, 64, 34, 128, 163, 94, 230, 128, 186, 8, 0, 0, 0, 0, 149, 0, 6, 241, 161, 10, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 94])
                }
                return null
            }
            ,
            t
        }();
        e.a = a
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = Math.pow(2, 32) - 1
          , n = function() {
            function t() {
                i(this, t)
            }
            return t.init = function() {
                t.types = {
                    avc1: [],
                    avcC: [],
                    btrt: [],
                    dinf: [],
                    dref: [],
                    esds: [],
                    ftyp: [],
                    hdlr: [],
                    mdat: [],
                    mdhd: [],
                    mdia: [],
                    mfhd: [],
                    minf: [],
                    moof: [],
                    moov: [],
                    mp4a: [],
                    ".mp3": [],
                    mvex: [],
                    mvhd: [],
                    pasp: [],
                    sdtp: [],
                    stbl: [],
                    stco: [],
                    stsc: [],
                    stsd: [],
                    stsz: [],
                    stts: [],
                    tfdt: [],
                    tfhd: [],
                    traf: [],
                    trak: [],
                    trun: [],
                    trex: [],
                    tkhd: [],
                    vmhd: [],
                    smhd: []
                };
                var e = void 0;
                for (e in t.types)
                    t.types.hasOwnProperty(e) && (t.types[e] = [e.charCodeAt(0), e.charCodeAt(1), e.charCodeAt(2), e.charCodeAt(3)]);
                var r = new Uint8Array([0, 0, 0, 0, 0, 0, 0, 0, 118, 105, 100, 101, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 86, 105, 100, 101, 111, 72, 97, 110, 100, 108, 101, 114, 0])
                  , i = new Uint8Array([0, 0, 0, 0, 0, 0, 0, 0, 115, 111, 117, 110, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 83, 111, 117, 110, 100, 72, 97, 110, 100, 108, 101, 114, 0]);
                t.HDLR_TYPES = {
                    video: r,
                    audio: i
                };
                var a = new Uint8Array([0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 12, 117, 114, 108, 32, 0, 0, 0, 1])
                  , n = new Uint8Array([0, 0, 0, 0, 0, 0, 0, 0]);
                t.STTS = t.STSC = t.STCO = n,
                t.STSZ = new Uint8Array([0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]),
                t.VMHD = new Uint8Array([0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0]),
                t.SMHD = new Uint8Array([0, 0, 0, 0, 0, 0, 0, 0]),
                t.STSD = new Uint8Array([0, 0, 0, 0, 0, 0, 0, 1]);
                var o = new Uint8Array([105, 115, 111, 109])
                  , s = new Uint8Array([97, 118, 99, 49])
                  , l = new Uint8Array([0, 0, 0, 1]);
                t.FTYP = t.box(t.types.ftyp, o, l, o, s),
                t.DINF = t.box(t.types.dinf, t.box(t.types.dref, a))
            }
            ,
            t.box = function(t) {
                for (var e = Array.prototype.slice.call(arguments, 1), r = 8, i = e.length, a = i, n = void 0; i--; )
                    r += e[i].byteLength;
                for (n = new Uint8Array(r),
                n[0] = r >> 24 & 255,
                n[1] = r >> 16 & 255,
                n[2] = r >> 8 & 255,
                n[3] = 255 & r,
                n.set(t, 4),
                i = 0,
                r = 8; i < a; i++)
                    n.set(e[i], r),
                    r += e[i].byteLength;
                return n
            }
            ,
            t.hdlr = function(e) {
                return t.box(t.types.hdlr, t.HDLR_TYPES[e])
            }
            ,
            t.mdat = function(e) {
                return t.box(t.types.mdat, e)
            }
            ,
            t.mdhd = function(e, r) {
                r *= e;
                var i = Math.floor(r / (a + 1))
                  , n = Math.floor(r % (a + 1));
                return t.box(t.types.mdhd, new Uint8Array([1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 3, e >> 24 & 255, e >> 16 & 255, e >> 8 & 255, 255 & e, i >> 24, i >> 16 & 255, i >> 8 & 255, 255 & i, n >> 24, n >> 16 & 255, n >> 8 & 255, 255 & n, 85, 196, 0, 0]))
            }
            ,
            t.mdia = function(e) {
                return t.box(t.types.mdia, t.mdhd(e.timescale, e.duration), t.hdlr(e.type), t.minf(e))
            }
            ,
            t.mfhd = function(e) {
                return t.box(t.types.mfhd, new Uint8Array([0, 0, 0, 0, e >> 24, e >> 16 & 255, e >> 8 & 255, 255 & e]))
            }
            ,
            t.minf = function(e) {
                return "audio" === e.type ? t.box(t.types.minf, t.box(t.types.smhd, t.SMHD), t.DINF, t.stbl(e)) : t.box(t.types.minf, t.box(t.types.vmhd, t.VMHD), t.DINF, t.stbl(e))
            }
            ,
            t.moof = function(e, r, i) {
                return t.box(t.types.moof, t.mfhd(e), t.traf(i, r))
            }
            ,
            t.moov = function(e) {
                for (var r = e.length, i = []; r--; )
                    i[r] = t.trak(e[r]);
                return t.box.apply(null, [t.types.moov, t.mvhd(e[0].timescale, e[0].duration)].concat(i).concat(t.mvex(e)))
            }
            ,
            t.mvex = function(e) {
                for (var r = e.length, i = []; r--; )
                    i[r] = t.trex(e[r]);
                return t.box.apply(null, [t.types.mvex].concat(i))
            }
            ,
            t.mvhd = function(e, r) {
                r *= e;
                var i = Math.floor(r / (a + 1))
                  , n = Math.floor(r % (a + 1))
                  , o = new Uint8Array([1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 3, e >> 24 & 255, e >> 16 & 255, e >> 8 & 255, 255 & e, i >> 24, i >> 16 & 255, i >> 8 & 255, 255 & i, n >> 24, n >> 16 & 255, n >> 8 & 255, 255 & n, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 64, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 255, 255, 255, 255]);
                return t.box(t.types.mvhd, o)
            }
            ,
            t.sdtp = function(e) {
                var r = e.samples || []
                  , i = new Uint8Array(4 + r.length)
                  , a = void 0
                  , n = void 0;
                for (n = 0; n < r.length; n++)
                    a = r[n].flags,
                    i[n + 4] = a.dependsOn << 4 | a.isDependedOn << 2 | a.hasRedundancy;
                return t.box(t.types.sdtp, i)
            }
            ,
            t.stbl = function(e) {
                return t.box(t.types.stbl, t.stsd(e), t.box(t.types.stts, t.STTS), t.box(t.types.stsc, t.STSC), t.box(t.types.stsz, t.STSZ), t.box(t.types.stco, t.STCO))
            }
            ,
            t.avc1 = function(e) {
                var r = []
                  , i = []
                  , a = void 0
                  , n = void 0
                  , o = void 0;
                for (a = 0; a < e.sps.length; a++)
                    n = e.sps[a],
                    o = n.byteLength,
                    r.push(o >>> 8 & 255),
                    r.push(255 & o),
                    r = r.concat(Array.prototype.slice.call(n));
                for (a = 0; a < e.pps.length; a++)
                    n = e.pps[a],
                    o = n.byteLength,
                    i.push(o >>> 8 & 255),
                    i.push(255 & o),
                    i = i.concat(Array.prototype.slice.call(n));
                var s = t.box(t.types.avcC, new Uint8Array([1, r[3], r[4], r[5], 255, 224 | e.sps.length].concat(r).concat([e.pps.length]).concat(i)))
                  , l = e.width
                  , u = e.height
                  , d = e.pixelRatio[0]
                  , c = e.pixelRatio[1];
                return t.box(t.types.avc1, new Uint8Array([0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, l >> 8 & 255, 255 & l, u >> 8 & 255, 255 & u, 0, 72, 0, 0, 0, 72, 0, 0, 0, 0, 0, 0, 0, 1, 18, 100, 97, 105, 108, 121, 109, 111, 116, 105, 111, 110, 47, 104, 108, 115, 46, 106, 115, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 24, 17, 17]), s, t.box(t.types.btrt, new Uint8Array([0, 28, 156, 128, 0, 45, 198, 192, 0, 45, 198, 192])), t.box(t.types.pasp, new Uint8Array([d >> 24, d >> 16 & 255, d >> 8 & 255, 255 & d, c >> 24, c >> 16 & 255, c >> 8 & 255, 255 & c])))
            }
            ,
            t.esds = function(t) {
                var e = t.config.length;
                return new Uint8Array([0, 0, 0, 0, 3, 23 + e, 0, 1, 0, 4, 15 + e, 64, 21, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 5].concat([e]).concat(t.config).concat([6, 1, 2]))
            }
            ,
            t.mp4a = function(e) {
                var r = e.samplerate;
                return t.box(t.types.mp4a, new Uint8Array([0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, e.channelCount, 0, 16, 0, 0, 0, 0, r >> 8 & 255, 255 & r, 0, 0]), t.box(t.types.esds, t.esds(e)))
            }
            ,
            t.mp3 = function(e) {
                var r = e.samplerate;
                return t.box(t.types[".mp3"], new Uint8Array([0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, e.channelCount, 0, 16, 0, 0, 0, 0, r >> 8 & 255, 255 & r, 0, 0]))
            }
            ,
            t.stsd = function(e) {
                return "audio" === e.type ? e.isAAC || "mp3" !== e.codec ? t.box(t.types.stsd, t.STSD, t.mp4a(e)) : t.box(t.types.stsd, t.STSD, t.mp3(e)) : t.box(t.types.stsd, t.STSD, t.avc1(e))
            }
            ,
            t.tkhd = function(e) {
                var r = e.id
                  , i = e.duration * e.timescale
                  , n = e.width
                  , o = e.height
                  , s = Math.floor(i / (a + 1))
                  , l = Math.floor(i % (a + 1));
                return t.box(t.types.tkhd, new Uint8Array([1, 0, 0, 7, 0, 0, 0, 0, 0, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 3, r >> 24 & 255, r >> 16 & 255, r >> 8 & 255, 255 & r, 0, 0, 0, 0, s >> 24, s >> 16 & 255, s >> 8 & 255, 255 & s, l >> 24, l >> 16 & 255, l >> 8 & 255, 255 & l, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 64, 0, 0, 0, n >> 8 & 255, 255 & n, 0, 0, o >> 8 & 255, 255 & o, 0, 0]))
            }
            ,
            t.traf = function(e, r) {
                var i = t.sdtp(e)
                  , n = e.id
                  , o = Math.floor(r / (a + 1))
                  , s = Math.floor(r % (a + 1));
                return t.box(t.types.traf, t.box(t.types.tfhd, new Uint8Array([0, 0, 0, 0, n >> 24, n >> 16 & 255, n >> 8 & 255, 255 & n])), t.box(t.types.tfdt, new Uint8Array([1, 0, 0, 0, o >> 24, o >> 16 & 255, o >> 8 & 255, 255 & o, s >> 24, s >> 16 & 255, s >> 8 & 255, 255 & s])), t.trun(e, i.length + 16 + 20 + 8 + 16 + 8 + 8), i)
            }
            ,
            t.trak = function(e) {
                return e.duration = e.duration || 4294967295,
                t.box(t.types.trak, t.tkhd(e), t.mdia(e))
            }
            ,
            t.trex = function(e) {
                var r = e.id;
                return t.box(t.types.trex, new Uint8Array([0, 0, 0, 0, r >> 24, r >> 16 & 255, r >> 8 & 255, 255 & r, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 1]))
            }
            ,
            t.trun = function(e, r) {
                var i = e.samples || []
                  , a = i.length
                  , n = 12 + 16 * a
                  , o = new Uint8Array(n)
                  , s = void 0
                  , l = void 0
                  , u = void 0
                  , d = void 0
                  , c = void 0
                  , h = void 0;
                for (r += 8 + n,
                o.set([0, 0, 15, 1, a >>> 24 & 255, a >>> 16 & 255, a >>> 8 & 255, 255 & a, r >>> 24 & 255, r >>> 16 & 255, r >>> 8 & 255, 255 & r], 0),
                s = 0; s < a; s++)
                    l = i[s],
                    u = l.duration,
                    d = l.size,
                    c = l.flags,
                    h = l.cts,
                    o.set([u >>> 24 & 255, u >>> 16 & 255, u >>> 8 & 255, 255 & u, d >>> 24 & 255, d >>> 16 & 255, d >>> 8 & 255, 255 & d, c.isLeading << 2 | c.dependsOn, c.isDependedOn << 6 | c.hasRedundancy << 4 | c.paddingValue << 1 | c.isNonSync, 61440 & c.degradPrio, 15 & c.degradPrio, h >>> 24 & 255, h >>> 16 & 255, h >>> 8 & 255, 255 & h], 12 + 16 * s);
                return t.box(t.types.trun, o)
            }
            ,
            t.initSegment = function(e) {
                t.types || t.init();
                var r = t.moov(e)
                  , i = void 0;
                return i = new Uint8Array(t.FTYP.byteLength + r.byteLength),
                i.set(t.FTYP),
                i.set(r, t.FTYP.byteLength),
                i
            }
            ,
            t
        }();
        e.a = n
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(1)
          , n = function() {
            function t(e) {
                i(this, t),
                this.observer = e
            }
            return t.prototype.destroy = function() {}
            ,
            t.prototype.resetTimeStamp = function() {}
            ,
            t.prototype.resetInitSegment = function() {}
            ,
            t.prototype.remux = function(t, e, r, i, n, o, s, l) {
                var u = this.observer
                  , d = "";
                t && (d += "audio"),
                e && (d += "video"),
                u.trigger(a.a.FRAG_PARSING_DATA, {
                    data1: l,
                    startPTS: n,
                    startDTS: n,
                    type: d,
                    hasAudio: !!t,
                    hasVideo: !!e,
                    nb: 1,
                    dropped: 0
                }),
                u.trigger(a.a.FRAG_PARSED)
            }
            ,
            t
        }();
        e.a = n
    }
    , function(t, e, r) {
        "use strict";
        Object.defineProperty(e, "__esModule", {
            value: !0
        });
        var i = r(22)
          , a = r(1)
          , n = r(0)
          , o = r(13)
          , s = r.n(o)
          , l = function(t) {
            var e = new s.a;
            e.trigger = function(t) {
                for (var r = arguments.length, i = Array(r > 1 ? r - 1 : 0), a = 1; a < r; a++)
                    i[a - 1] = arguments[a];
                e.emit.apply(e, [t, t].concat(i))
            }
            ,
            e.off = function(t) {
                for (var r = arguments.length, i = Array(r > 1 ? r - 1 : 0), a = 1; a < r; a++)
                    i[a - 1] = arguments[a];
                e.removeListener.apply(e, [t].concat(i))
            }
            ;
            var r = function(e, r) {
                t.postMessage({
                    event: e,
                    data: r
                })
            };
            t.addEventListener("message", function(a) {
                var o = a.data;
                switch (o.cmd) {
                case "init":
                    var s = JSON.parse(o.config);
                    t.demuxer = new i.a(e,o.typeSupported,s,o.vendor);
                    try {
                        Object(n.a)(!0 === s.debug)
                    } catch (t) {
                        console.warn("demuxerWorker: unable to enable logs")
                    }
                    r("init", null);
                    break;
                case "demux":
                    t.demuxer.push(o.data, o.decryptdata, o.initSegment, o.audioCodec, o.videoCodec, o.timeOffset, o.discontinuity, o.trackSwitch, o.contiguous, o.duration, o.accurateTimeOffset, o.defaultInitPTS)
                }
            }),
            e.on(a.a.FRAG_DECRYPTED, r),
            e.on(a.a.FRAG_PARSING_INIT_SEGMENT, r),
            e.on(a.a.FRAG_PARSED, r),
            e.on(a.a.ERROR, r),
            e.on(a.a.FRAG_PARSING_METADATA, r),
            e.on(a.a.FRAG_PARSING_USERDATA, r),
            e.on(a.a.INIT_PTS_FOUND, r),
            e.on(a.a.FRAG_PARSING_DATA, function(e, r) {
                var i = []
                  , a = {
                    event: e,
                    data: r
                };
                r.data1 && (a.data1 = r.data1.buffer,
                i.push(r.data1.buffer),
                delete r.data1),
                r.data2 && (a.data2 = r.data2.buffer,
                i.push(r.data2.buffer),
                delete r.data2),
                t.postMessage(a, i)
            })
        };
        e.default = l
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e, r) {
            if (!Array.isArray(t) || !t.length || !Object(s.a)(e))
                return null;
            if (e < t[0].programDateTime)
                return null;
            if (e >= t[t.length - 1].endProgramDateTime)
                return null;
            r = r || 0;
            for (var i = 0; i < t.length; ++i) {
                var a = t[i];
                if (o(e, r, a))
                    return a
            }
            return null
        }
        function a(t, e) {
            var r = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : 0
              , i = arguments.length > 3 && void 0 !== arguments[3] ? arguments[3] : 0
              , a = t ? e[t.sn - e[0].sn + 1] : null;
            return a && !n(r, i, a) ? a : l.a.search(e, n.bind(null, r, i))
        }
        function n() {
            var t = arguments.length > 0 && void 0 !== arguments[0] ? arguments[0] : 0
              , e = arguments.length > 1 && void 0 !== arguments[1] ? arguments[1] : 0
              , r = arguments[2]
              , i = Math.min(e, r.duration + (r.deltaPTS ? r.deltaPTS : 0));
            return r.start + r.duration - i <= t ? 1 : r.start - i > t && r.start ? -1 : 0
        }
        function o(t, e, r) {
            var i = 1e3 * Math.min(e, r.duration + (r.deltaPTS ? r.deltaPTS : 0));
            return r.endProgramDateTime - i > t
        }
        e.a = i,
        e.b = a;
        var s = r(3)
          , l = r(7)
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(8)
          , n = r(2)
          , o = r(1)
          , s = r(0)
          , l = function() {
            function t(e, r, a, n) {
                i(this, t),
                this.config = e,
                this.media = r,
                this.fragmentTracker = a,
                this.hls = n,
                this.stallReported = !1
            }
            return t.prototype.poll = function(t, e) {
                var r = this.config
                  , i = this.media
                  , n = i.currentTime
                  , o = window.performance.now();
                if (n !== t)
                    return this.stallReported && (s.b.warn("playback not stuck anymore @" + n + ", after " + Math.round(o - this.stalled) + "ms"),
                    this.stallReported = !1),
                    this.stalled = null,
                    void (this.nudgeRetry = 0);
                if (!(i.ended || !i.buffered.length || i.readyState > 2 || i.seeking && a.a.isBuffered(i, n))) {
                    var l = o - this.stalled
                      , u = a.a.bufferInfo(i, n, r.maxBufferHole);
                    if (!this.stalled)
                        return void (this.stalled = o);
                    l >= 1e3 && this._reportStall(u.len),
                    this._tryFixBufferStall(u, l)
                }
            }
            ,
            t.prototype._tryFixBufferStall = function(t, e) {
                var r = this.config
                  , i = this.fragmentTracker
                  , a = this.media
                  , n = a.currentTime
                  , o = i.getPartialFragment(n);
                o && this._trySkipBufferHole(o),
                t.len > .5 && e > 1e3 * r.highBufferWatchdogPeriod && (this.stalled = null,
                this._tryNudgeBuffer())
            }
            ,
            t.prototype._reportStall = function(t) {
                var e = this.hls
                  , r = this.media;
                this.stallReported || (this.stallReported = !0,
                s.b.warn("Playback stalling at @" + r.currentTime + " due to low buffer"),
                e.trigger(o.a.ERROR, {
                    type: n.b.MEDIA_ERROR,
                    details: n.a.BUFFER_STALLED_ERROR,
                    fatal: !1,
                    buffer: t
                }))
            }
            ,
            t.prototype._trySkipBufferHole = function(t) {
                for (var e = this.hls, r = this.media, i = r.currentTime, a = 0, l = 0; l < r.buffered.length; l++) {
                    var u = r.buffered.start(l);
                    if (i >= a && i < u)
                        return r.currentTime = Math.max(u, r.currentTime + .1),
                        s.b.warn("skipping hole, adjusting currentTime from " + i + " to " + r.currentTime),
                        this.stalled = null,
                        void e.trigger(o.a.ERROR, {
                            type: n.b.MEDIA_ERROR,
                            details: n.a.BUFFER_SEEK_OVER_HOLE,
                            fatal: !1,
                            reason: "fragment loaded with buffer holes, seeking from " + i + " to " + r.currentTime,
                            frag: t
                        });
                    a = r.buffered.end(l)
                }
            }
            ,
            t.prototype._tryNudgeBuffer = function() {
                var t = this.config
                  , e = this.hls
                  , r = this.media
                  , i = r.currentTime
                  , a = (this.nudgeRetry || 0) + 1;
                if (this.nudgeRetry = a,
                a < t.nudgeMaxRetry) {
                    var l = i + a * t.nudgeOffset;
                    s.b.log("adjust currentTime from " + i + " to " + l),
                    r.currentTime = l,
                    e.trigger(o.a.ERROR, {
                        type: n.b.MEDIA_ERROR,
                        details: n.a.BUFFER_NUDGE_ON_STALL,
                        fatal: !1
                    })
                } else
                    s.b.error("still stuck in high buffer @" + i + " after " + t.nudgeMaxRetry + ", raise fatal error"),
                    e.trigger(o.a.ERROR, {
                        type: n.b.MEDIA_ERROR,
                        details: n.a.BUFFER_STALLED_ERROR,
                        fatal: !0
                    })
            }
            ,
            t
        }();
        e.a = l
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(1)
          , s = r(4)
          , l = r(0)
          , u = r(2)
          , d = r(20)
          , c = r(16)
          , h = "function" == typeof Symbol && "symbol" == typeof Symbol.iterator ? function(t) {
            return typeof t
        }
        : function(t) {
            return t && "function" == typeof Symbol && t.constructor === Symbol && t !== Symbol.prototype ? "symbol" : typeof t
        }
          , f = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , p = window
          , g = p.performance
          , v = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, o.a.MANIFEST_LOADED, o.a.LEVEL_LOADED, o.a.AUDIO_TRACK_SWITCHED, o.a.FRAG_LOADED, o.a.ERROR));
                return n.canload = !1,
                n.currentLevelIndex = null,
                n.manualLevelIndex = -1,
                n.timer = null,
                n
            }
            return n(e, t),
            e.prototype.onHandlerDestroying = function() {
                this.clearTimer(),
                this.manualLevelIndex = -1
            }
            ,
            e.prototype.clearTimer = function() {
                null !== this.timer && (clearTimeout(this.timer),
                this.timer = null)
            }
            ,
            e.prototype.startLoad = function() {
                var t = this._levels;
                this.canload = !0,
                this.levelRetryCount = 0,
                t && t.forEach(function(t) {
                    t.loadError = 0;
                    var e = t.details;
                    e && e.live && (t.details = void 0)
                }),
                null !== this.timer && this.loadLevel()
            }
            ,
            e.prototype.stopLoad = function() {
                this.canload = !1
            }
            ,
            e.prototype.onManifestLoaded = function(t) {
                var e = []
                  , r = void 0
                  , i = {}
                  , a = null
                  , n = !1
                  , s = !1
                  , h = /chrome|firefox/.test(navigator.userAgent.toLowerCase())
                  , f = [];
                if (t.levels.forEach(function(t) {
                    t.loadError = 0,
                    t.fragmentError = !1,
                    n = n || !!t.videoCodec,
                    s = s || !!t.audioCodec || !(!t.attrs || !t.attrs.AUDIO),
                    h && t.audioCodec && -1 !== t.audioCodec.indexOf("mp4a.40.34") && (t.audioCodec = void 0),
                    a = i[t.bitrate],
                    a ? a.url.push(t.url) : (t.url = [t.url],
                    t.urlId = 0,
                    i[t.bitrate] = t,
                    e.push(t)),
                    t.attrs && t.attrs.AUDIO && Object(c.a)(a || t, "audio", t.attrs.AUDIO),
                    t.attrs && t.attrs.SUBTITLES && Object(c.a)(a || t, "text", t.attrs.SUBTITLES)
                }),
                n && s && (e = e.filter(function(t) {
                    return !!t.videoCodec
                })),
                e = e.filter(function(t) {
                    var e = t.audioCodec
                      , r = t.videoCodec;
                    return (!e || Object(d.a)(e)) && (!r || Object(d.a)(r))
                }),
                t.audioTracks && (f = t.audioTracks.filter(function(t) {
                    return !t.audioCodec || Object(d.a)(t.audioCodec, "audio")
                }),
                f.forEach(function(t, e) {
                    t.id = e
                })),
                e.length > 0) {
                    r = e[0].bitrate,
                    e.sort(function(t, e) {
                        return t.bitrate - e.bitrate
                    }),
                    this._levels = e;
                    for (var p = 0; p < e.length; p++)
                        if (e[p].bitrate === r) {
                            this._firstLevel = p,
                            l.b.log("manifest loaded," + e.length + " level(s) found, first bitrate:" + r);
                            break
                        }
                    this.hls.trigger(o.a.MANIFEST_PARSED, {
                        levels: e,
                        audioTracks: f,
                        firstLevel: this._firstLevel,
                        stats: t.stats,
                        audio: s,
                        video: n,
                        altAudio: f.length > 0 && n
                    })
                } else
                    this.hls.trigger(o.a.ERROR, {
                        type: u.b.MEDIA_ERROR,
                        details: u.a.MANIFEST_INCOMPATIBLE_CODECS_ERROR,
                        fatal: !0,
                        url: this.hls.url,
                        reason: "no level with compatible codecs found in manifest"
                    })
            }
            ,
            e.prototype.setLevelInternal = function(t) {
                var e = this._levels
                  , r = this.hls;
                if (t >= 0 && t < e.length) {
                    if (this.clearTimer(),
                    this.currentLevelIndex !== t) {
                        l.b.log("switching to level " + t),
                        this.currentLevelIndex = t;
                        var i = e[t];
                        i.level = t,
                        r.trigger(o.a.LEVEL_SWITCHING, i)
                    }
                    var a = e[t]
                      , n = a.details;
                    if (!n || n.live) {
                        var s = a.urlId;
                        r.trigger(o.a.LEVEL_LOADING, {
                            url: a.url[s],
                            level: t,
                            id: s
                        })
                    }
                } else
                    r.trigger(o.a.ERROR, {
                        type: u.b.OTHER_ERROR,
                        details: u.a.LEVEL_SWITCH_ERROR,
                        level: t,
                        fatal: !1,
                        reason: "invalid level idx"
                    })
            }
            ,
            e.prototype.onError = function(t) {
                if (t.fatal)
                    return void (t.type === u.b.NETWORK_ERROR && this.clearTimer());
                var e = !1
                  , r = !1
                  , i = void 0;
                switch (t.details) {
                case u.a.FRAG_LOAD_ERROR:
                case u.a.FRAG_LOAD_TIMEOUT:
                case u.a.KEY_LOAD_ERROR:
                case u.a.KEY_LOAD_TIMEOUT:
                    i = t.frag.level,
                    r = !0;
                    break;
                case u.a.LEVEL_LOAD_ERROR:
                case u.a.LEVEL_LOAD_TIMEOUT:
                    i = t.context.level,
                    e = !0;
                    break;
                case u.a.REMUX_ALLOC_ERROR:
                    i = t.level,
                    e = !0
                }
                void 0 !== i && this.recoverLevel(t, i, e, r)
            }
            ,
            e.prototype.recoverLevel = function(t, e, r, i) {
                var a = this
                  , n = this.hls.config
                  , o = t.details
                  , s = this._levels[e]
                  , u = void 0
                  , d = void 0
                  , c = void 0;
                if (s.loadError++,
                s.fragmentError = i,
                r) {
                    if (!(this.levelRetryCount + 1 <= n.levelLoadingMaxRetry))
                        return l.b.error("level controller, cannot recover from " + o + " error"),
                        this.currentLevelIndex = null,
                        this.clearTimer(),
                        void (t.fatal = !0);
                    d = Math.min(Math.pow(2, this.levelRetryCount) * n.levelLoadingRetryDelay, n.levelLoadingMaxRetryTimeout),
                    this.timer = setTimeout(function() {
                        return a.loadLevel()
                    }, d),
                    t.levelRetry = !0,
                    this.levelRetryCount++,
                    l.b.warn("level controller, " + o + ", retry in " + d + " ms, current retry count is " + this.levelRetryCount)
                }
                (r || i) && (u = s.url.length,
                u > 1 && s.loadError < u ? (s.urlId = (s.urlId + 1) % u,
                s.details = void 0,
                l.b.warn("level controller, " + o + " for level " + e + ": switching to redundant URL-id " + s.urlId)) : -1 === this.manualLevelIndex ? (c = 0 === e ? this._levels.length - 1 : e - 1,
                l.b.warn("level controller, " + o + ": switch to " + c),
                this.hls.nextAutoLevel = this.currentLevelIndex = c) : i && (l.b.warn("level controller, " + o + ": reload a fragment"),
                this.currentLevelIndex = null))
            }
            ,
            e.prototype.onFragLoaded = function(t) {
                var e = t.frag;
                if (void 0 !== e && "main" === e.type) {
                    var r = this._levels[e.level];
                    void 0 !== r && (r.fragmentError = !1,
                    r.loadError = 0,
                    this.levelRetryCount = 0)
                }
            }
            ,
            e.prototype.onLevelLoaded = function(t) {
                var e = this
                  , r = t.level;
                if (r === this.currentLevelIndex) {
                    var i = this._levels[r];
                    i.fragmentError || (i.loadError = 0,
                    this.levelRetryCount = 0);
                    var a = t.details;
                    if (a.live) {
                        var n = 1e3 * (a.averagetargetduration ? a.averagetargetduration : a.targetduration)
                          , o = n
                          , s = i.details;
                        s && a.endSN === s.endSN && (o /= 2,
                        l.b.log("same live playlist, reload twice faster")),
                        o -= g.now() - t.stats.trequest,
                        o = Math.max(n / 2, Math.round(o)),
                        l.b.log("live playlist, reload in " + Math.round(o) + " ms"),
                        this.timer = setTimeout(function() {
                            return e.loadLevel()
                        }, o)
                    } else
                        this.clearTimer()
                }
            }
            ,
            e.prototype.onAudioTrackSwitched = function(t) {
                var e = this.hls.audioTracks[t.id].groupId
                  , r = this.hls.levels[this.currentLevelIndex];
                if (r && r.audioGroupIds) {
                    var i = r.audioGroupIds.findIndex(function(t) {
                        return t === e
                    });
                    i !== r.urlId && (r.urlId = i,
                    this.startLoad())
                }
            }
            ,
            e.prototype.loadLevel = function() {
                if (l.b.debug("call to loadLevel"),
                null !== this.currentLevelIndex && this.canload) {
                    var t = this._levels[this.currentLevelIndex];
                    if ("object" === (void 0 === t ? "undefined" : h(t)) && t.url.length > 0) {
                        var e = this.currentLevelIndex
                          , r = t.urlId
                          , i = t.url[r];
                        l.b.log("Attempt loading level index " + e + " with URL-id " + r),
                        this.hls.trigger(o.a.LEVEL_LOADING, {
                            url: i,
                            level: e,
                            id: r
                        })
                    }
                }
            }
            ,
            f(e, [{
                key: "levels",
                get: function() {
                    return this._levels
                }
            }, {
                key: "level",
                get: function() {
                    return this.currentLevelIndex
                },
                set: function(t) {
                    var e = this._levels;
                    e && (t = Math.min(t, e.length - 1),
                    this.currentLevelIndex === t && e[t].details || this.setLevelInternal(t))
                }
            }, {
                key: "manualLevel",
                get: function() {
                    return this.manualLevelIndex
                },
                set: function(t) {
                    this.manualLevelIndex = t,
                    void 0 === this._startLevel && (this._startLevel = t),
                    -1 !== t && (this.level = t)
                }
            }, {
                key: "firstLevel",
                get: function() {
                    return this._firstLevel
                },
                set: function(t) {
                    this._firstLevel = t
                }
            }, {
                key: "startLevel",
                get: function() {
                    if (void 0 === this._startLevel) {
                        var t = this.hls.config.startLevel;
                        return void 0 !== t ? t : this._firstLevel
                    }
                    return this._startLevel
                },
                set: function(t) {
                    this._startLevel = t
                }
            }, {
                key: "nextLoadLevel",
                get: function() {
                    return -1 !== this.manualLevelIndex ? this.manualLevelIndex : this.hls.nextAutoLevel
                },
                set: function(t) {
                    this.level = t,
                    -1 === this.manualLevelIndex && (this.hls.nextAutoLevel = t)
                }
            }]),
            e
        }(s.a);
        e.a = v
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(1)
          , s = r(4)
          , l = r(9)
          , u = r(27)
          , d = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, o.a.MEDIA_ATTACHED, o.a.MEDIA_DETACHING, o.a.FRAG_PARSING_METADATA));
                return n.id3Track = void 0,
                n.media = void 0,
                n
            }
            return n(e, t),
            e.prototype.destroy = function() {
                s.a.prototype.destroy.call(this)
            }
            ,
            e.prototype.onMediaAttached = function(t) {
                this.media = t.media,
                this.media
            }
            ,
            e.prototype.onMediaDetaching = function() {
                Object(u.a)(this.id3Track),
                this.id3Track = void 0,
                this.media = void 0
            }
            ,
            e.prototype.getID3Track = function(t) {
                for (var e = 0; e < t.length; e++) {
                    var r = t[e];
                    if ("metadata" === r.kind && "id3" === r.label)
                        return Object(u.b)(r, this.media),
                        r
                }
                return this.media.addTextTrack("metadata", "id3")
            }
            ,
            e.prototype.onFragParsingMetadata = function(t) {
                var e = t.frag
                  , r = t.samples;
                this.id3Track || (this.id3Track = this.getID3Track(this.media.textTracks),
                this.id3Track.mode = "hidden");
                for (var i = window.WebKitDataCue || window.VTTCue || window.TextTrackCue, a = 0; a < r.length; a++) {
                    var n = l.a.getID3Frames(r[a].data);
                    if (n) {
                        var o = r[a].pts
                          , s = a < r.length - 1 ? r[a + 1].pts : e.endPTS;
                        o === s && (s += 1e-4);
                        for (var u = 0; u < n.length; u++) {
                            var d = n[u];
                            if (!l.a.isTimeStampFrame(d)) {
                                var c = new i(o,s,"");
                                c.value = d,
                                this.id3Track.addCue(c)
                            }
                        }
                    }
                }
            }
            ,
            e
        }(s.a);
        e.a = d
    }
    , function(t, e, r) {
        "use strict";
        function i() {
            var t = Object(a.a)()
              , e = window.SourceBuffer || window.WebKitSourceBuffer
              , r = t && "function" == typeof t.isTypeSupported && t.isTypeSupported('video/mp4; codecs="avc1.42E01E,mp4a.40.2"')
              , i = !e || e.prototype && "function" == typeof e.prototype.appendBuffer && "function" == typeof e.prototype.remove;
            return !!r && !!i
        }
        e.a = i;
        var a = r(15)
    }
    , function(t, e, r) {
        "use strict";
        r.d(e, "a", function() {
            return v
        });
        var i = r(56)
          , a = r(59)
          , n = r(60)
          , o = r(61)
          , s = r(62)
          , l = r(63)
          , u = r(64)
          , d = r(65)
          , c = r(67)
          , h = r(71)
          , f = r(72)
          , p = r(73)
          , g = r(74)
          , v = {
            autoStartLoad: !0,
            startPosition: -1,
            defaultAudioCodec: void 0,
            debug: !1,
            capLevelOnFPSDrop: !1,
            capLevelToPlayerSize: !1,
            initialLiveManifestSize: 1,
            maxBufferLength: 30,
            maxBufferSize: 6e7,
            maxBufferHole: .5,
            lowBufferWatchdogPeriod: .5,
            highBufferWatchdogPeriod: 3,
            nudgeOffset: .1,
            nudgeMaxRetry: 3,
            maxFragLookUpTolerance: .25,
            liveSyncDurationCount: 3,
            liveMaxLatencyDurationCount: 1 / 0,
            liveSyncDuration: void 0,
            liveMaxLatencyDuration: void 0,
            liveDurationInfinity: !1,
            maxMaxBufferLength: 600,
            enableWorker: !0,
            enableSoftwareAES: !0,
            manifestLoadingTimeOut: 1e4,
            manifestLoadingMaxRetry: 1,
            manifestLoadingRetryDelay: 1e3,
            manifestLoadingMaxRetryTimeout: 64e3,
            startLevel: void 0,
            levelLoadingTimeOut: 1e4,
            levelLoadingMaxRetry: 4,
            levelLoadingRetryDelay: 1e3,
            levelLoadingMaxRetryTimeout: 64e3,
            fragLoadingTimeOut: 2e4,
            fragLoadingMaxRetry: 6,
            fragLoadingRetryDelay: 1e3,
            fragLoadingMaxRetryTimeout: 64e3,
            startFragPrefetch: !1,
            fpsDroppedMonitoringPeriod: 5e3,
            fpsDroppedMonitoringThreshold: .2,
            appendErrorMaxRetry: 3,
            loader: s.a,
            fLoader: void 0,
            pLoader: void 0,
            xhrSetup: void 0,
            licenseXhrSetup: void 0,
            abrController: i.a,
            bufferController: a.a,
            capLevelController: n.a,
            fpsController: o.a,
            stretchShortVideoTrack: !1,
            maxAudioFramesDrift: 1,
            forceKeyFrameOnDiscontinuity: !0,
            abrEwmaFastLive: 3,
            abrEwmaSlowLive: 9,
            abrEwmaFastVoD: 3,
            abrEwmaSlowVoD: 9,
            abrEwmaDefaultEstimate: 5e5,
            abrBandWidthFactor: .95,
            abrBandWidthUpFactor: .7,
            abrMaxWithRealBitrate: !1,
            maxStarvationDelay: 4,
            maxLoadingDelay: 4,
            minAutoBitrate: 0,
            emeEnabled: !1,
            widevineLicenseUrl: void 0,
            requestMediaKeySystemAccessFunc: g.a
        };
        v.subtitleStreamController = f.a,
        v.subtitleTrackController = h.a,
        v.timelineController = c.a,
        v.cueHandler = d,
        v.enableCEA708Captions = !0,
        v.enableWebVTT = !0,
        v.captionsTextTrack1Label = "English",
        v.captionsTextTrack1LanguageCode = "en",
        v.captionsTextTrack2Label = "Spanish",
        v.captionsTextTrack2LanguageCode = "es",
        v.audioStreamController = u.a,
        v.audioTrackController = l.a,
        v.emeController = p.a
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(3)
          , s = r(1)
          , l = r(4)
          , u = r(8)
          , d = r(2)
          , c = r(0)
          , h = r(57)
          , f = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , p = window
          , g = p.performance
          , v = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, s.a.FRAG_LOADING, s.a.FRAG_LOADED, s.a.FRAG_BUFFERED, s.a.ERROR));
                return n.lastLoadedFragLevel = 0,
                n._nextAutoLevel = -1,
                n.hls = r,
                n.timer = null,
                n._bwEstimator = null,
                n.onCheck = n._abandonRulesCheck.bind(n),
                n
            }
            return n(e, t),
            e.prototype.destroy = function() {
                this.clearTimer(),
                l.a.prototype.destroy.call(this)
            }
            ,
            e.prototype.onFragLoading = function(t) {
                var e = t.frag;
                if ("main" === e.type && (this.timer || (this.fragCurrent = e,
                this.timer = setInterval(this.onCheck, 100)),
                !this._bwEstimator)) {
                    var r = this.hls
                      , i = r.config
                      , a = e.level
                      , n = r.levels[a].details.live
                      , o = void 0
                      , s = void 0;
                    n ? (o = i.abrEwmaFastLive,
                    s = i.abrEwmaSlowLive) : (o = i.abrEwmaFastVoD,
                    s = i.abrEwmaSlowVoD),
                    this._bwEstimator = new h.a(r,s,o,i.abrEwmaDefaultEstimate)
                }
            }
            ,
            e.prototype._abandonRulesCheck = function() {
                var t = this.hls
                  , e = t.media
                  , r = this.fragCurrent;
                if (r) {
                    var i = r.loader
                      , a = t.minAutoLevel;
                    if (!i || i.stats && i.stats.aborted)
                        return c.b.warn("frag loader destroy or aborted, disarm abandonRules"),
                        this.clearTimer(),
                        void (this._nextAutoLevel = -1);
                    var n = i.stats;
                    if (e && n && (!e.paused && 0 !== e.playbackRate || !e.readyState) && r.autoLevel && r.level) {
                        var o = g.now() - n.trequest
                          , l = Math.abs(e.playbackRate);
                        if (o > 500 * r.duration / l) {
                            var d = t.levels
                              , h = Math.max(1, n.bw ? n.bw / 8 : 1e3 * n.loaded / o)
                              , f = d[r.level]
                              , p = f.realBitrate ? Math.max(f.realBitrate, f.bitrate) : f.bitrate
                              , v = n.total ? n.total : Math.max(n.loaded, Math.round(r.duration * p / 8))
                              , y = e.currentTime
                              , m = (v - n.loaded) / h
                              , b = (u.a.bufferInfo(e, y, t.config.maxBufferHole).end - y) / l;
                            if (b < 2 * r.duration / l && m > b) {
                                var E = void 0
                                  , T = void 0;
                                for (T = r.level - 1; T > a; T--) {
                                    var S = d[T].realBitrate ? Math.max(d[T].realBitrate, d[T].bitrate) : d[T].bitrate;
                                    if ((E = r.duration * S / (6.4 * h)) < b)
                                        break
                                }
                                E < m && (c.b.warn("loading too slow, abort fragment loading and switch to level " + T + ":fragLoadedDelay[" + T + "]<fragLoadedDelay[" + (r.level - 1) + "];bufferStarvationDelay:" + E.toFixed(1) + "<" + m.toFixed(1) + ":" + b.toFixed(1)),
                                t.nextLoadLevel = T,
                                this._bwEstimator.sample(o, n.loaded),
                                i.abort(),
                                this.clearTimer(),
                                t.trigger(s.a.FRAG_LOAD_EMERGENCY_ABORTED, {
                                    frag: r,
                                    stats: n
                                }))
                            }
                        }
                    }
                }
            }
            ,
            e.prototype.onFragLoaded = function(t) {
                var e = t.frag;
                if ("main" === e.type && Object(o.a)(e.sn)) {
                    if (this.clearTimer(),
                    this.lastLoadedFragLevel = e.level,
                    this._nextAutoLevel = -1,
                    this.hls.config.abrMaxWithRealBitrate) {
                        var r = this.hls.levels[e.level]
                          , i = (r.loaded ? r.loaded.bytes : 0) + t.stats.loaded
                          , a = (r.loaded ? r.loaded.duration : 0) + t.frag.duration;
                        r.loaded = {
                            bytes: i,
                            duration: a
                        },
                        r.realBitrate = Math.round(8 * i / a)
                    }
                    if (t.frag.bitrateTest) {
                        var n = t.stats;
                        n.tparsed = n.tbuffered = n.tload,
                        this.onFragBuffered(t)
                    }
                }
            }
            ,
            e.prototype.onFragBuffered = function(t) {
                var e = t.stats
                  , r = t.frag;
                if (!0 !== e.aborted && "main" === r.type && Object(o.a)(r.sn) && (!r.bitrateTest || e.tload === e.tbuffered)) {
                    var i = e.tparsed - e.trequest;
                    c.b.log("latency/loading/parsing/append/kbps:" + Math.round(e.tfirst - e.trequest) + "/" + Math.round(e.tload - e.tfirst) + "/" + Math.round(e.tparsed - e.tload) + "/" + Math.round(e.tbuffered - e.tparsed) + "/" + Math.round(8 * e.loaded / (e.tbuffered - e.trequest))),
                    this._bwEstimator.sample(i, e.loaded),
                    e.bwEstimate = this._bwEstimator.getEstimate(),
                    r.bitrateTest ? this.bitrateTestDelay = i / 1e3 : this.bitrateTestDelay = 0
                }
            }
            ,
            e.prototype.onError = function(t) {
                switch (t.details) {
                case d.a.FRAG_LOAD_ERROR:
                case d.a.FRAG_LOAD_TIMEOUT:
                    this.clearTimer()
                }
            }
            ,
            e.prototype.clearTimer = function() {
                clearInterval(this.timer),
                this.timer = null
            }
            ,
            e.prototype._findBestLevel = function(t, e, r, i, a, n, o, s, l) {
                for (var u = a; u >= i; u--) {
                    var d = l[u];
                    if (d) {
                        var h = d.details
                          , f = h ? h.totalduration / h.fragments.length : e
                          , p = !!h && h.live
                          , g = void 0;
                        g = u <= t ? o * r : s * r;
                        var v = l[u].realBitrate ? Math.max(l[u].realBitrate, l[u].bitrate) : l[u].bitrate
                          , y = v * f / g;
                        if (c.b.trace("level/adjustedbw/bitrate/avgDuration/maxFetchDuration/fetchDuration: " + u + "/" + Math.round(g) + "/" + v + "/" + f + "/" + n + "/" + y),
                        g > v && (!y || p && !this.bitrateTestDelay || y < n))
                            return u
                    }
                }
                return -1
            }
            ,
            f(e, [{
                key: "nextAutoLevel",
                get: function() {
                    var t = this._nextAutoLevel
                      , e = this._bwEstimator;
                    if (!(-1 === t || e && e.canEstimate()))
                        return t;
                    var r = this._nextABRAutoLevel;
                    return -1 !== t && (r = Math.min(t, r)),
                    r
                },
                set: function(t) {
                    this._nextAutoLevel = t
                }
            }, {
                key: "_nextABRAutoLevel",
                get: function() {
                    var t = this.hls
                      , e = t.maxAutoLevel
                      , r = t.levels
                      , i = t.config
                      , a = t.minAutoLevel
                      , n = t.media
                      , o = this.lastLoadedFragLevel
                      , s = this.fragCurrent ? this.fragCurrent.duration : 0
                      , l = n ? n.currentTime : 0
                      , d = n && 0 !== n.playbackRate ? Math.abs(n.playbackRate) : 1
                      , h = this._bwEstimator ? this._bwEstimator.getEstimate() : i.abrEwmaDefaultEstimate
                      , f = (u.a.bufferInfo(n, l, i.maxBufferHole).end - l) / d
                      , p = this._findBestLevel(o, s, h, a, e, f, i.abrBandWidthFactor, i.abrBandWidthUpFactor, r);
                    if (p >= 0)
                        return p;
                    c.b.trace("rebuffering expected to happen, lets try to find a quality level minimizing the rebuffering");
                    var g = s ? Math.min(s, i.maxStarvationDelay) : i.maxStarvationDelay
                      , v = i.abrBandWidthFactor
                      , y = i.abrBandWidthUpFactor;
                    if (0 === f) {
                        var m = this.bitrateTestDelay;
                        if (m) {
                            g = (s ? Math.min(s, i.maxLoadingDelay) : i.maxLoadingDelay) - m,
                            c.b.trace("bitrate test took " + Math.round(1e3 * m) + "ms, set first fragment max fetchDuration to " + Math.round(1e3 * g) + " ms"),
                            v = y = 1
                        }
                    }
                    return p = this._findBestLevel(o, s, h, a, e, f + g, v, y, r),
                    Math.max(p, 0)
                }
            }]),
            e
        }(l.a);
        e.a = v
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(58)
          , n = function() {
            function t(e, r, n, o) {
                i(this, t),
                this.hls = e,
                this.defaultEstimate_ = o,
                this.minWeight_ = .001,
                this.minDelayMs_ = 50,
                this.slow_ = new a.a(r),
                this.fast_ = new a.a(n)
            }
            return t.prototype.sample = function(t, e) {
                t = Math.max(t, this.minDelayMs_);
                var r = 8e3 * e / t
                  , i = t / 1e3;
                this.fast_.sample(i, r),
                this.slow_.sample(i, r)
            }
            ,
            t.prototype.canEstimate = function() {
                var t = this.fast_;
                return t && t.getTotalWeight() >= this.minWeight_
            }
            ,
            t.prototype.getEstimate = function() {
                return this.canEstimate() ? Math.min(this.fast_.getEstimate(), this.slow_.getEstimate()) : this.defaultEstimate_
            }
            ,
            t.prototype.destroy = function() {}
            ,
            t
        }();
        e.a = n
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = function() {
            function t(e) {
                i(this, t),
                this.alpha_ = e ? Math.exp(Math.log(.5) / e) : 0,
                this.estimate_ = 0,
                this.totalWeight_ = 0
            }
            return t.prototype.sample = function(t, e) {
                var r = Math.pow(this.alpha_, t);
                this.estimate_ = e * (1 - r) + r * this.estimate_,
                this.totalWeight_ += t
            }
            ,
            t.prototype.getTotalWeight = function() {
                return this.totalWeight_
            }
            ,
            t.prototype.getEstimate = function() {
                if (this.alpha_) {
                    var t = 1 - Math.pow(this.alpha_, this.totalWeight_);
                    return this.estimate_ / t
                }
                return this.estimate_
            }
            ,
            t
        }();
        e.a = a
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(3)
          , s = r(1)
          , l = r(4)
          , u = r(0)
          , d = r(2)
          , c = r(15)
          , h = Object(c.a)()
          , f = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, s.a.MEDIA_ATTACHING, s.a.MEDIA_DETACHING, s.a.MANIFEST_PARSED, s.a.BUFFER_RESET, s.a.BUFFER_APPENDING, s.a.BUFFER_CODECS, s.a.BUFFER_EOS, s.a.BUFFER_FLUSHING, s.a.LEVEL_PTS_UPDATED, s.a.LEVEL_UPDATED));
                return n._msDuration = null,
                n._levelDuration = null,
                n._live = null,
                n._objectUrl = null,
                n.onsbue = n.onSBUpdateEnd.bind(n),
                n.onsbe = n.onSBUpdateError.bind(n),
                n.pendingTracks = {},
                n.tracks = {},
                n
            }
            return n(e, t),
            e.prototype.destroy = function() {
                l.a.prototype.destroy.call(this)
            }
            ,
            e.prototype.onLevelPtsUpdated = function(t) {
                var e = t.type
                  , r = this.tracks.audio;
                if ("audio" === e && r && "audio/mpeg" === r.container) {
                    var i = this.sourceBuffer.audio;
                    if (Math.abs(i.timestampOffset - t.start) > .1) {
                        var a = i.updating;
                        try {
                            i.abort()
                        } catch (t) {
                            a = !0,
                            u.b.warn("can not abort audio buffer: " + t)
                        }
                        a ? this.audioTimestampOffset = t.start : (u.b.warn("change mpeg audio timestamp offset from " + i.timestampOffset + " to " + t.start),
                        i.timestampOffset = t.start)
                    }
                }
            }
            ,
            e.prototype.onManifestParsed = function(t) {
                var e = t.audio
                  , r = t.video || t.levels.length && t.altAudio
                  , i = 0;
                t.altAudio && (e || r) && (i = (e ? 1 : 0) + (r ? 1 : 0),
                u.b.log(i + " sourceBuffer(s) expected")),
                this.sourceBufferNb = i
            }
            ,
            e.prototype.onMediaAttaching = function(t) {
                var e = this.media = t.media;
                if (e) {
                    var r = this.mediaSource = new h;
                    this.onmso = this.onMediaSourceOpen.bind(this),
                    this.onmse = this.onMediaSourceEnded.bind(this),
                    this.onmsc = this.onMediaSourceClose.bind(this),
                    r.addEventListener("sourceopen", this.onmso),
                    r.addEventListener("sourceended", this.onmse),
                    r.addEventListener("sourceclose", this.onmsc),
                    e.src = window.URL.createObjectURL(r),
                    this._objectUrl = e.src
                }
            }
            ,
            e.prototype.onMediaDetaching = function() {
                u.b.log("media source detaching");
                var t = this.mediaSource;
                if (t) {
                    if ("open" === t.readyState)
                        try {
                            t.endOfStream()
                        } catch (t) {
                            u.b.warn("onMediaDetaching:" + t.message + " while calling endOfStream")
                        }
                    t.removeEventListener("sourceopen", this.onmso),
                    t.removeEventListener("sourceended", this.onmse),
                    t.removeEventListener("sourceclose", this.onmsc),
                    this.media && (window.URL.revokeObjectURL(this._objectUrl),
                    this.media.src === this._objectUrl ? (this.media.removeAttribute("src"),
                    this.media.load()) : u.b.warn("media.src was changed by a third party - skip cleanup")),
                    this.mediaSource = null,
                    this.media = null,
                    this._objectUrl = null,
                    this.pendingTracks = {},
                    this.tracks = {},
                    this.sourceBuffer = {},
                    this.flushRange = [],
                    this.segments = [],
                    this.appended = 0
                }
                this.onmso = this.onmse = this.onmsc = null,
                this.hls.trigger(s.a.MEDIA_DETACHED)
            }
            ,
            e.prototype.onMediaSourceOpen = function() {
                u.b.log("media source opened"),
                this.hls.trigger(s.a.MEDIA_ATTACHED, {
                    media: this.media
                });
                var t = this.mediaSource;
                t && t.removeEventListener("sourceopen", this.onmso),
                this.checkPendingTracks()
            }
            ,
            e.prototype.checkPendingTracks = function() {
                var t = this.pendingTracks
                  , e = Object.keys(t).length;
                e && (this.sourceBufferNb <= e || 0 === this.sourceBufferNb) && (this.createSourceBuffers(t),
                this.pendingTracks = {},
                this.doAppending())
            }
            ,
            e.prototype.onMediaSourceClose = function() {
                u.b.log("media source closed")
            }
            ,
            e.prototype.onMediaSourceEnded = function() {
                u.b.log("media source ended")
            }
            ,
            e.prototype.onSBUpdateEnd = function() {
                if (this.audioTimestampOffset) {
                    var t = this.sourceBuffer.audio;
                    u.b.warn("change mpeg audio timestamp offset from " + t.timestampOffset + " to " + this.audioTimestampOffset),
                    t.timestampOffset = this.audioTimestampOffset,
                    delete this.audioTimestampOffset
                }
                this._needsFlush && this.doFlush(),
                this._needsEos && this.checkEos(),
                this.appending = !1;
                var e = this.parent
                  , r = this.segments.reduce(function(t, r) {
                    return r.parent === e ? t + 1 : t
                }, 0)
                  , i = {}
                  , a = this.sourceBuffer;
                for (var n in a)
                    i[n] = a[n].buffered;
                this.hls.trigger(s.a.BUFFER_APPENDED, {
                    parent: e,
                    pending: r,
                    timeRanges: i
                }),
                this._needsFlush || this.doAppending(),
                this.updateMediaElementDuration()
            }
            ,
            e.prototype.onSBUpdateError = function(t) {
                u.b.error("sourceBuffer error:", t),
                this.hls.trigger(s.a.ERROR, {
                    type: d.b.MEDIA_ERROR,
                    details: d.a.BUFFER_APPENDING_ERROR,
                    fatal: !1
                })
            }
            ,
            e.prototype.onBufferReset = function() {
                var t = this.sourceBuffer;
                for (var e in t) {
                    var r = t[e];
                    try {
                        this.mediaSource.removeSourceBuffer(r),
                        r.removeEventListener("updateend", this.onsbue),
                        r.removeEventListener("error", this.onsbe)
                    } catch (t) {}
                }
                this.sourceBuffer = {},
                this.flushRange = [],
                this.segments = [],
                this.appended = 0
            }
            ,
            e.prototype.onBufferCodecs = function(t) {
                if (0 === Object.keys(this.sourceBuffer).length) {
                    for (var e in t)
                        this.pendingTracks[e] = t[e];
                    var r = this.mediaSource;
                    r && "open" === r.readyState && this.checkPendingTracks()
                }
            }
            ,
            e.prototype.createSourceBuffers = function(t) {
                var e = this.sourceBuffer
                  , r = this.mediaSource;
                for (var i in t)
                    if (!e[i]) {
                        var a = t[i]
                          , n = a.levelCodec || a.codec
                          , o = a.container + ";codecs=" + n;
                        u.b.log("creating sourceBuffer(" + o + ")");
                        try {
                            var l = e[i] = r.addSourceBuffer(o);
                            l.addEventListener("updateend", this.onsbue),
                            l.addEventListener("error", this.onsbe),
                            this.tracks[i] = {
                                codec: n,
                                container: a.container
                            },
                            a.buffer = l
                        } catch (t) {
                            u.b.error("error while trying to add sourceBuffer:" + t.message),
                            this.hls.trigger(s.a.ERROR, {
                                type: d.b.MEDIA_ERROR,
                                details: d.a.BUFFER_ADD_CODEC_ERROR,
                                fatal: !1,
                                err: t,
                                mimeType: o
                            })
                        }
                    }
                this.hls.trigger(s.a.BUFFER_CREATED, {
                    tracks: t
                })
            }
            ,
            e.prototype.onBufferAppending = function(t) {
                this._needsFlush || (this.segments ? this.segments.push(t) : this.segments = [t],
                this.doAppending())
            }
            ,
            e.prototype.onBufferAppendFail = function(t) {
                u.b.error("sourceBuffer error:", t.event),
                this.hls.trigger(s.a.ERROR, {
                    type: d.b.MEDIA_ERROR,
                    details: d.a.BUFFER_APPENDING_ERROR,
                    fatal: !1
                })
            }
            ,
            e.prototype.onBufferEos = function(t) {
                var e = this.sourceBuffer
                  , r = t.type;
                for (var i in e)
                    r && i !== r || e[i].ended || (e[i].ended = !0,
                    u.b.log(i + " sourceBuffer now EOS"));
                this.checkEos()
            }
            ,
            e.prototype.checkEos = function() {
                var t = this.sourceBuffer
                  , e = this.mediaSource;
                if (!e || "open" !== e.readyState)
                    return void (this._needsEos = !1);
                for (var r in t) {
                    var i = t[r];
                    if (!i.ended)
                        return;
                    if (i.updating)
                        return void (this._needsEos = !0)
                }
                u.b.log("all media data available, signal endOfStream() to MediaSource and stop loading fragment");
                try {
                    e.endOfStream()
                } catch (t) {
                    u.b.warn("exception while calling mediaSource.endOfStream()")
                }
                this._needsEos = !1
            }
            ,
            e.prototype.onBufferFlushing = function(t) {
                this.flushRange.push({
                    start: t.startOffset,
                    end: t.endOffset,
                    type: t.type
                }),
                this.flushBufferCounter = 0,
                this.doFlush()
            }
            ,
            e.prototype.onLevelUpdated = function(t) {
                var e = t.details;
                e.fragments.length > 0 && (this._levelDuration = e.totalduration + e.fragments[0].start,
                this._live = e.live,
                this.updateMediaElementDuration())
            }
            ,
            e.prototype.updateMediaElementDuration = function() {
                var t = this.hls.config
                  , e = void 0;
                if (null !== this._levelDuration && this.media && this.mediaSource && this.sourceBuffer && 0 !== this.media.readyState && "open" === this.mediaSource.readyState) {
                    for (var r in this.sourceBuffer)
                        if (!0 === this.sourceBuffer[r].updating)
                            return;
                    e = this.media.duration,
                    null === this._msDuration && (this._msDuration = this.mediaSource.duration),
                    !0 === this._live && !0 === t.liveDurationInfinity ? (u.b.log("Media Source duration is set to Infinity"),
                    this._msDuration = this.mediaSource.duration = 1 / 0) : (this._levelDuration > this._msDuration && this._levelDuration > e || !Object(o.a)(e)) && (u.b.log("Updating Media Source duration to " + this._levelDuration.toFixed(3)),
                    this._msDuration = this.mediaSource.duration = this._levelDuration)
                }
            }
            ,
            e.prototype.doFlush = function() {
                for (; this.flushRange.length; ) {
                    var t = this.flushRange[0];
                    if (!this.flushBuffer(t.start, t.end, t.type))
                        return void (this._needsFlush = !0);
                    this.flushRange.shift(),
                    this.flushBufferCounter = 0
                }
                if (0 === this.flushRange.length) {
                    this._needsFlush = !1;
                    var e = 0
                      , r = this.sourceBuffer;
                    try {
                        for (var i in r)
                            e += r[i].buffered.length
                    } catch (t) {
                        u.b.error("error while accessing sourceBuffer.buffered")
                    }
                    this.appended = e,
                    this.hls.trigger(s.a.BUFFER_FLUSHED)
                }
            }
            ,
            e.prototype.doAppending = function() {
                var t = this.hls
                  , e = this.sourceBuffer
                  , r = this.segments;
                if (Object.keys(e).length) {
                    if (this.media.error)
                        return this.segments = [],
                        void u.b.error("trying to append although a media error occured, flush segment and abort");
                    if (this.appending)
                        return;
                    if (r && r.length) {
                        var i = r.shift();
                        try {
                            var a = i.type
                              , n = e[a];
                            n ? n.updating ? r.unshift(i) : (n.ended = !1,
                            this.parent = i.parent,
                            n.appendBuffer(i.data),
                            this.appendError = 0,
                            this.appended++,
                            this.appending = !0) : this.onSBUpdateEnd()
                        } catch (e) {
                            u.b.error("error while trying to append buffer:" + e.message),
                            r.unshift(i);
                            var o = {
                                type: d.b.MEDIA_ERROR,
                                parent: i.parent
                            };
                            22 !== e.code ? (this.appendError ? this.appendError++ : this.appendError = 1,
                            o.details = d.a.BUFFER_APPEND_ERROR,
                            this.appendError > t.config.appendErrorMaxRetry ? (u.b.log("fail " + t.config.appendErrorMaxRetry + " times to append segment in sourceBuffer"),
                            r = [],
                            o.fatal = !0,
                            t.trigger(s.a.ERROR, o)) : (o.fatal = !1,
                            t.trigger(s.a.ERROR, o))) : (this.segments = [],
                            o.details = d.a.BUFFER_FULL_ERROR,
                            o.fatal = !1,
                            t.trigger(s.a.ERROR, o))
                        }
                    }
                }
            }
            ,
            e.prototype.flushBuffer = function(t, e, r) {
                var i = void 0
                  , a = void 0
                  , n = void 0
                  , o = void 0
                  , s = void 0
                  , l = void 0
                  , d = this.sourceBuffer;
                if (Object.keys(d).length) {
                    if (u.b.log("flushBuffer,pos/start/end: " + this.media.currentTime.toFixed(3) + "/" + t + "/" + e),
                    this.flushBufferCounter < this.appended) {
                        for (var c in d)
                            if (!r || c === r) {
                                if (i = d[c],
                                i.ended = !1,
                                i.updating)
                                    return u.b.warn("cannot flush, sb updating in progress"),
                                    !1;
                                try {
                                    for (a = 0; a < i.buffered.length; a++)
                                        if (n = i.buffered.start(a),
                                        o = i.buffered.end(a),
                                        -1 !== navigator.userAgent.toLowerCase().indexOf("firefox") && e === Number.POSITIVE_INFINITY ? (s = t,
                                        l = e) : (s = Math.max(n, t),
                                        l = Math.min(o, e)),
                                        Math.min(l, o) - s > .5)
                                            return this.flushBufferCounter++,
                                            u.b.log("flush " + c + " [" + s + "," + l + "], of [" + n + "," + o + "], pos:" + this.media.currentTime),
                                            i.remove(s, l),
                                            !1
                                } catch (t) {
                                    u.b.warn("exception while accessing sourcebuffer, it might have been removed from MediaSource")
                                }
                            }
                    } else
                        u.b.warn("abort flushing too many retries");
                    u.b.log("buffer flushed")
                }
                return !0
            }
            ,
            e
        }(l.a);
        e.a = f
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(1)
          , s = r(4)
          , l = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , u = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, o.a.FPS_DROP_LEVEL_CAPPING, o.a.MEDIA_ATTACHING, o.a.MANIFEST_PARSED, o.a.BUFFER_CODECS, o.a.MEDIA_DETACHING));
                return n.autoLevelCapping = Number.POSITIVE_INFINITY,
                n.firstLevel = null,
                n.levels = [],
                n.media = null,
                n.restrictedLevels = [],
                n.timer = null,
                n
            }
            return n(e, t),
            e.prototype.destroy = function() {
                this.hls.config.capLevelToPlayerSize && (this.media = null,
                this._stopCapping())
            }
            ,
            e.prototype.onFpsDropLevelCapping = function(t) {
                e.isLevelAllowed(t.droppedLevel, this.restrictedLevels) && this.restrictedLevels.push(t.droppedLevel)
            }
            ,
            e.prototype.onMediaAttaching = function(t) {
                this.media = t.media instanceof window.HTMLVideoElement ? t.media : null
            }
            ,
            e.prototype.onManifestParsed = function(t) {
                var e = this.hls;
                this.restrictedLevels = [],
                this.levels = t.levels,
                this.firstLevel = t.firstLevel,
                e.config.capLevelToPlayerSize && (t.video || t.levels.length && t.altAudio) && this._startCapping()
            }
            ,
            e.prototype.onBufferCodecs = function(t) {
                this.hls.config.capLevelToPlayerSize && t.video && this._startCapping()
            }
            ,
            e.prototype.onLevelsUpdated = function(t) {
                this.levels = t.levels
            }
            ,
            e.prototype.onMediaDetaching = function() {
                this._stopCapping()
            }
            ,
            e.prototype.detectPlayerSize = function() {
                if (this.media) {
                    var t = this.levels ? this.levels.length : 0;
                    if (t) {
                        var e = this.hls;
                        e.autoLevelCapping = this.getMaxLevel(t - 1),
                        e.autoLevelCapping > this.autoLevelCapping && e.streamController.nextLevelSwitch(),
                        this.autoLevelCapping = e.autoLevelCapping
                    }
                }
            }
            ,
            e.prototype.getMaxLevel = function(t) {
                var r = this;
                if (!this.levels)
                    return -1;
                var i = this.levels.filter(function(i, a) {
                    return e.isLevelAllowed(a, r.restrictedLevels) && a <= t
                });
                return e.getMaxLevelByMediaSize(i, this.mediaWidth, this.mediaHeight)
            }
            ,
            e.prototype._startCapping = function() {
                this.timer || (this.autoLevelCapping = Number.POSITIVE_INFINITY,
                this.hls.firstLevel = this.getMaxLevel(this.firstLevel),
                clearInterval(this.timer),
                this.timer = setInterval(this.detectPlayerSize.bind(this), 1e3),
                this.detectPlayerSize())
            }
            ,
            e.prototype._stopCapping = function() {
                this.restrictedLevels = [],
                this.firstLevel = null,
                this.autoLevelCapping = Number.POSITIVE_INFINITY,
                this.timer && (this.timer = clearInterval(this.timer),
                this.timer = null)
            }
            ,
            e.isLevelAllowed = function(t) {
                return -1 === (arguments.length > 1 && void 0 !== arguments[1] ? arguments[1] : []).indexOf(t)
            }
            ,
            e.getMaxLevelByMediaSize = function(t, e, r) {
                if (!t || t && !t.length)
                    return -1;
                for (var i = t.length - 1, a = 0; a < t.length; a += 1) {
                    var n = t[a];
                    if ((n.width >= e || n.height >= r) && function(t, e) {
                        return !e || (t.width !== e.width || t.height !== e.height)
                    }(n, t[a + 1])) {
                        i = a;
                        break
                    }
                }
                return i
            }
            ,
            l(e, [{
                key: "mediaWidth",
                get: function() {
                    var t = void 0
                      , r = this.media;
                    return r && (t = r.width || r.clientWidth || r.offsetWidth,
                    t *= e.contentScaleFactor),
                    t
                }
            }, {
                key: "mediaHeight",
                get: function() {
                    var t = void 0
                      , r = this.media;
                    return r && (t = r.height || r.clientHeight || r.offsetHeight,
                    t *= e.contentScaleFactor),
                    t
                }
            }], [{
                key: "contentScaleFactor",
                get: function() {
                    var t = 1;
                    try {
                        t = window.devicePixelRatio
                    } catch (t) {}
                    return t
                }
            }]),
            e
        }(s.a);
        e.a = u
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(1)
          , s = r(4)
          , l = r(0)
          , u = window
          , d = u.performance
          , c = function(t) {
            function e(r) {
                return i(this, e),
                a(this, t.call(this, r, o.a.MEDIA_ATTACHING))
            }
            return n(e, t),
            e.prototype.destroy = function() {
                this.timer && clearInterval(this.timer),
                this.isVideoPlaybackQualityAvailable = !1
            }
            ,
            e.prototype.onMediaAttaching = function(t) {
                var e = this.hls.config;
                if (e.capLevelOnFPSDrop) {
                    "function" == typeof (this.video = t.media instanceof window.HTMLVideoElement ? t.media : null).getVideoPlaybackQuality && (this.isVideoPlaybackQualityAvailable = !0),
                    clearInterval(this.timer),
                    this.timer = setInterval(this.checkFPSInterval.bind(this), e.fpsDroppedMonitoringPeriod)
                }
            }
            ,
            e.prototype.checkFPS = function(t, e, r) {
                var i = d.now();
                if (e) {
                    if (this.lastTime) {
                        var a = i - this.lastTime
                          , n = r - this.lastDroppedFrames
                          , s = e - this.lastDecodedFrames
                          , u = 1e3 * n / a
                          , c = this.hls;
                        if (c.trigger(o.a.FPS_DROP, {
                            currentDropped: n,
                            currentDecoded: s,
                            totalDroppedFrames: r
                        }),
                        u > 0 && n > c.config.fpsDroppedMonitoringThreshold * s) {
                            var h = c.currentLevel;
                            l.b.warn("drop FPS ratio greater than max allowed value for currentLevel: " + h),
                            h > 0 && (-1 === c.autoLevelCapping || c.autoLevelCapping >= h) && (h -= 1,
                            c.trigger(o.a.FPS_DROP_LEVEL_CAPPING, {
                                level: h,
                                droppedLevel: c.currentLevel
                            }),
                            c.autoLevelCapping = h,
                            c.streamController.nextLevelSwitch())
                        }
                    }
                    this.lastTime = i,
                    this.lastDroppedFrames = r,
                    this.lastDecodedFrames = e
                }
            }
            ,
            e.prototype.checkFPSInterval = function() {
                var t = this.video;
                if (t)
                    if (this.isVideoPlaybackQualityAvailable) {
                        var e = t.getVideoPlaybackQuality();
                        this.checkFPS(t, e.totalVideoFrames, e.droppedVideoFrames)
                    } else
                        this.checkFPS(t, t.webkitDecodedFrameCount, t.webkitDroppedFrameCount)
            }
            ,
            e
        }(s.a);
        e.a = c
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = r(0)
          , n = window
          , o = n.performance
          , s = n.XMLHttpRequest
          , l = function() {
            function t(e) {
                i(this, t),
                e && e.xhrSetup && (this.xhrSetup = e.xhrSetup)
            }
            return t.prototype.destroy = function() {
                this.abort(),
                this.loader = null
            }
            ,
            t.prototype.abort = function() {
                var t = this.loader;
                t && 4 !== t.readyState && (this.stats.aborted = !0,
                t.abort()),
                window.clearTimeout(this.requestTimeout),
                this.requestTimeout = null,
                window.clearTimeout(this.retryTimeout),
                this.retryTimeout = null
            }
            ,
            t.prototype.load = function(t, e, r) {
                this.context = t,
                this.config = e,
                this.callbacks = r,
                this.stats = {
                    trequest: o.now(),
                    retry: 0
                },
                this.retryDelay = e.retryDelay,
                this.loadInternal()
            }
            ,
            t.prototype.loadInternal = function() {
                var t = void 0
                  , e = this.context;
                t = this.loader = new s;
                var r = this.stats;
                r.tfirst = 0,
                r.loaded = 0;
                var i = this.xhrSetup;
                try {
                    if (i)
                        try {
                            i(t, e.url)
                        } catch (r) {
                            t.open("GET", e.url, !0),
                            i(t, e.url)
                        }
                    t.readyState || t.open("GET", e.url, !0)
                } catch (r) {
                    return void this.callbacks.onError({
                        code: t.status,
                        text: r.message
                    }, e, t)
                }
                e.rangeEnd && t.setRequestHeader("Range", "bytes=" + e.rangeStart + "-" + (e.rangeEnd - 1)),
                t.onreadystatechange = this.readystatechange.bind(this),
                t.onprogress = this.loadprogress.bind(this),
                t.responseType = e.responseType,
                this.requestTimeout = window.setTimeout(this.loadtimeout.bind(this), this.config.timeout),
                t.send()
            }
            ,
            t.prototype.readystatechange = function(t) {
                var e = t.currentTarget
                  , r = e.readyState
                  , i = this.stats
                  , n = this.context
                  , s = this.config;
                if (!i.aborted && r >= 2)
                    if (window.clearTimeout(this.requestTimeout),
                    0 === i.tfirst && (i.tfirst = Math.max(o.now(), i.trequest)),
                    4 === r) {
                        var l = e.status;
                        if (l >= 200 && l < 300) {
                            i.tload = Math.max(i.tfirst, o.now());
                            var u = void 0
                              , d = void 0;
                            "arraybuffer" === n.responseType ? (u = e.response,
                            d = u.byteLength) : (u = e.responseText,
                            d = u.length),
                            i.loaded = i.total = d;
                            var c = {
                                url: e.responseURL,
                                data: u
                            };
                            this.callbacks.onSuccess(c, i, n, e)
                        } else
                            i.retry >= s.maxRetry || l >= 400 && l < 499 ? (a.b.error(l + " while loading " + n.url),
                            this.callbacks.onError({
                                code: l,
                                text: e.statusText
                            }, n, e)) : (a.b.warn(l + " while loading " + n.url + ", retrying in " + this.retryDelay + "..."),
                            this.destroy(),
                            this.retryTimeout = window.setTimeout(this.loadInternal.bind(this), this.retryDelay),
                            this.retryDelay = Math.min(2 * this.retryDelay, s.maxRetryDelay),
                            i.retry++)
                    } else
                        this.requestTimeout = window.setTimeout(this.loadtimeout.bind(this), s.timeout)
            }
            ,
            t.prototype.loadtimeout = function() {
                a.b.warn("timeout while loading " + this.context.url),
                this.callbacks.onTimeout(this.stats, this.context, null)
            }
            ,
            t.prototype.loadprogress = function(t) {
                var e = t.currentTarget
                  , r = this.stats;
                r.loaded = t.loaded,
                t.lengthComputable && (r.total = t.total);
                var i = this.callbacks.onProgress;
                i && i(r, this.context, null, e)
            }
            ,
            t
        }();
        e.a = l
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(1)
          , s = r(10)
          , l = r(0)
          , u = r(2)
          , d = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , c = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, o.a.MANIFEST_LOADING, o.a.MANIFEST_PARSED, o.a.AUDIO_TRACK_LOADED, o.a.AUDIO_TRACK_SWITCHED, o.a.LEVEL_LOADED, o.a.ERROR));
                return n._trackId = -1,
                n._selectDefaultTrack = !0,
                n.tracks = [],
                n.trackIdBlacklist = Object.create(null),
                n.audioGroupId = null,
                n
            }
            return n(e, t),
            e.prototype.onManifestLoading = function() {
                this.tracks = [],
                this._trackId = -1,
                this._selectDefaultTrack = !0
            }
            ,
            e.prototype.onManifestParsed = function(t) {
                var e = this.tracks = t.audioTracks || [];
                this.hls.trigger(o.a.AUDIO_TRACKS_UPDATED, {
                    audioTracks: e
                })
            }
            ,
            e.prototype.onAudioTrackLoaded = function(t) {
                if (t.id >= this.tracks.length)
                    return void l.b.warn("Invalid audio track id:", t.id);
                if (l.b.log("audioTrack " + t.id + " loaded"),
                this.tracks[t.id].details = t.details,
                t.details.live && !this.hasInterval()) {
                    var e = 1e3 * t.details.targetduration;
                    this.setInterval(e)
                }
                !t.details.live && this.hasInterval() && this.clearInterval()
            }
            ,
            e.prototype.onAudioTrackSwitched = function(t) {
                var e = this.tracks[t.id].groupId;
                e && this.audioGroupId !== e && (this.audioGroupId = e)
            }
            ,
            e.prototype.onLevelLoaded = function(t) {
                var e = this.hls.levels[t.level];
                if (e.audioGroupIds) {
                    var r = e.audioGroupIds[e.urlId];
                    this.audioGroupId !== r && (this.audioGroupId = r,
                    this._selectInitialAudioTrack())
                }
            }
            ,
            e.prototype.onError = function(t) {
                t.type === u.b.NETWORK_ERROR && (t.fatal && this.clearInterval(),
                t.details === u.a.AUDIO_TRACK_LOAD_ERROR && (l.b.warn("Network failure on audio-track id:", t.context.id),
                this._handleLoadError()))
            }
            ,
            e.prototype._setAudioTrack = function(t) {
                if (this._trackId === t && this.tracks[this._trackId].details)
                    return void l.b.debug("Same id as current audio-track passed, and track details available -> no-op");
                if (t < 0 || t >= this.tracks.length)
                    return void l.b.warn("Invalid id passed to audio-track controller");
                var e = this.tracks[t];
                l.b.log("Now switching to audio-track index " + t),
                this.clearInterval(),
                this._trackId = t;
                var r = e.url
                  , i = e.type
                  , a = e.id;
                this.hls.trigger(o.a.AUDIO_TRACK_SWITCHING, {
                    id: a,
                    type: i,
                    url: r
                }),
                this._loadTrackDetailsIfNeeded(e)
            }
            ,
            e.prototype.doTick = function() {
                this._updateTrack(this._trackId)
            }
            ,
            e.prototype._selectInitialAudioTrack = function() {
                var t = this
                  , e = this.tracks;
                if (e.length) {
                    var r = this.tracks[this._trackId]
                      , i = null;
                    if (r && (i = r.name),
                    this._selectDefaultTrack) {
                        var a = e.filter(function(t) {
                            return t.default
                        });
                        a.length ? e = a : l.b.warn("No default audio tracks defined")
                    }
                    var n = !1
                      , s = function() {
                        e.forEach(function(e) {
                            n || t.audioGroupId && e.groupId !== t.audioGroupId || i && i !== e.name || (t._setAudioTrack(e.id),
                            n = !0)
                        })
                    };
                    s(),
                    n || (i = null,
                    s()),
                    n || (l.b.error("No track found for running audio group-ID: " + this.audioGroupId),
                    this.hls.trigger(o.a.ERROR, {
                        type: u.b.MEDIA_ERROR,
                        details: u.a.AUDIO_TRACK_LOAD_ERROR,
                        fatal: !0
                    }))
                }
            }
            ,
            e.prototype._needsTrackLoading = function(t) {
                var e = t.details;
                return !e || (!!e.live || void 0)
            }
            ,
            e.prototype._loadTrackDetailsIfNeeded = function(t) {
                if (this._needsTrackLoading(t)) {
                    var e = t.url
                      , r = t.id;
                    l.b.log("loading audio-track playlist for id: " + r),
                    this.hls.trigger(o.a.AUDIO_TRACK_LOADING, {
                        url: e,
                        id: r
                    })
                }
            }
            ,
            e.prototype._updateTrack = function(t) {
                if (!(t < 0 || t >= this.tracks.length)) {
                    this.clearInterval(),
                    this._trackId = t,
                    l.b.log("trying to update audio-track " + t);
                    var e = this.tracks[t];
                    this._loadTrackDetailsIfNeeded(e)
                }
            }
            ,
            e.prototype._handleLoadError = function() {
                this.trackIdBlacklist[this._trackId] = !0;
                var t = this._trackId
                  , e = this.tracks[t]
                  , r = e.name
                  , i = e.language
                  , a = e.groupId;
                l.b.warn("Loading failed on audio track id: " + t + ", group-id: " + a + ', name/language: "' + r + '" / "' + i + '"');
                for (var n = t, o = 0; o < this.tracks.length; o++)
                    if (!this.trackIdBlacklist[o]) {
                        var s = this.tracks[o];
                        if (s.name === r) {
                            n = o;
                            break
                        }
                    }
                if (n === t)
                    return void l.b.warn('No fallback audio-track found for name/language: "' + r + '" / "' + i + '"');
                l.b.log("Attempting audio-track fallback id:", n, "group-id:", this.tracks[n].groupId),
                this._setAudioTrack(n)
            }
            ,
            d(e, [{
                key: "audioTracks",
                get: function() {
                    return this.tracks
                }
            }, {
                key: "audioTrack",
                get: function() {
                    return this._trackId
                },
                set: function(t) {
                    this._setAudioTrack(t),
                    this._selectDefaultTrack = !1
                }
            }]),
            e
        }(s.a);
        e.a = c
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(3)
          , s = r(7)
          , l = r(8)
          , u = r(21)
          , d = r(1)
          , c = r(16)
          , h = r(25)
          , f = r(2)
          , p = r(0)
          , g = r(26)
          , v = r(10)
          , y = r(12)
          , m = r(11)
          , b = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , E = window
          , T = E.performance
          , S = {
            STOPPED: "STOPPED",
            STARTING: "STARTING",
            IDLE: "IDLE",
            PAUSED: "PAUSED",
            KEY_LOADING: "KEY_LOADING",
            FRAG_LOADING: "FRAG_LOADING",
            FRAG_LOADING_WAITING_RETRY: "FRAG_LOADING_WAITING_RETRY",
            WAITING_TRACK: "WAITING_TRACK",
            PARSING: "PARSING",
            PARSED: "PARSED",
            BUFFER_FLUSHING: "BUFFER_FLUSHING",
            ENDED: "ENDED",
            ERROR: "ERROR",
            WAITING_INIT_PTS: "WAITING_INIT_PTS"
        }
          , A = function(t) {
            function e(r, n) {
                i(this, e);
                var o = a(this, t.call(this, r, d.a.MEDIA_ATTACHED, d.a.MEDIA_DETACHING, d.a.AUDIO_TRACKS_UPDATED, d.a.AUDIO_TRACK_SWITCHING, d.a.AUDIO_TRACK_LOADED, d.a.KEY_LOADED, d.a.FRAG_LOADED, d.a.FRAG_PARSING_INIT_SEGMENT, d.a.FRAG_PARSING_DATA, d.a.FRAG_PARSED, d.a.ERROR, d.a.BUFFER_RESET, d.a.BUFFER_CREATED, d.a.BUFFER_APPENDED, d.a.BUFFER_FLUSHED, d.a.INIT_PTS_FOUND));
                return o.fragmentTracker = n,
                o.config = r.config,
                o.audioCodecSwap = !1,
                o._state = S.STOPPED,
                o.initPTS = [],
                o.waitingFragment = null,
                o.videoTrackCC = null,
                o
            }
            return n(e, t),
            e.prototype.onHandlerDestroying = function() {
                this.stopLoad(),
                t.prototype.onHandlerDestroying.call(this)
            }
            ,
            e.prototype.onHandlerDestroyed = function() {
                this.state = S.STOPPED,
                this.fragmentTracker = null,
                t.prototype.onHandlerDestroyed.call(this)
            }
            ,
            e.prototype.onInitPtsFound = function(t) {
                var e = t.id
                  , r = t.frag.cc
                  , i = t.initPTS;
                "main" === e && (this.initPTS[r] = i,
                this.videoTrackCC = r,
                p.b.log("InitPTS for cc: " + r + " found from video track: " + i),
                this.state === S.WAITING_INIT_PTS && this.tick())
            }
            ,
            e.prototype.startLoad = function(t) {
                if (this.tracks) {
                    var e = this.lastCurrentTime;
                    this.stopLoad(),
                    this.setInterval(100),
                    this.fragLoadError = 0,
                    e > 0 && -1 === t ? (p.b.log("audio:override startPosition with lastCurrentTime @" + e.toFixed(3)),
                    this.state = S.IDLE) : (this.lastCurrentTime = this.startPosition ? this.startPosition : t,
                    this.state = S.STARTING),
                    this.nextLoadPosition = this.startPosition = this.lastCurrentTime,
                    this.tick()
                } else
                    this.startPosition = t,
                    this.state = S.STOPPED
            }
            ,
            e.prototype.stopLoad = function() {
                var t = this.fragCurrent;
                t && (t.loader && t.loader.abort(),
                this.fragmentTracker.removeFragment(t),
                this.fragCurrent = null),
                this.fragPrevious = null,
                this.demuxer && (this.demuxer.destroy(),
                this.demuxer = null),
                this.state = S.STOPPED
            }
            ,
            e.prototype.doTick = function() {
                var t = void 0
                  , e = void 0
                  , r = void 0
                  , i = this.hls
                  , a = i.config;
                switch (this.state) {
                case S.ERROR:
                case S.PAUSED:
                case S.BUFFER_FLUSHING:
                    break;
                case S.STARTING:
                    this.state = S.WAITING_TRACK,
                    this.loadedmetadata = !1;
                    break;
                case S.IDLE:
                    var n = this.tracks;
                    if (!n)
                        break;
                    if (!this.media && (this.startFragRequested || !a.startFragPrefetch))
                        break;
                    if (this.loadedmetadata)
                        t = this.media.currentTime;
                    else if (void 0 === (t = this.nextLoadPosition))
                        break;
                    var u = this.mediaBuffer ? this.mediaBuffer : this.media
                      , c = this.videoBuffer ? this.videoBuffer : this.media
                      , h = l.a.bufferInfo(u, t, a.maxBufferHole)
                      , f = l.a.bufferInfo(c, t, a.maxBufferHole)
                      , v = h.len
                      , m = h.end
                      , b = this.fragPrevious
                      , E = Math.min(a.maxBufferLength, a.maxMaxBufferLength)
                      , A = Math.max(E, f.len)
                      , R = this.audioSwitch
                      , _ = this.trackId;
                    if ((v < A || R) && _ < n.length) {
                        if (void 0 === (r = n[_].details)) {
                            this.state = S.WAITING_TRACK;
                            break
                        }
                        if (!R && !r.live && b && b.sn === r.endSN && !h.nextStart && (!this.media.seeking || this.media.duration - m < b.duration / 2)) {
                            this.hls.trigger(d.a.BUFFER_EOS, {
                                type: "audio"
                            }),
                            this.state = S.ENDED;
                            break
                        }
                        var w = r.fragments
                          , L = w.length
                          , D = w[0].start
                          , I = w[L - 1].start + w[L - 1].duration
                          , k = void 0;
                        if (R)
                            if (r.live && !r.PTSKnown)
                                p.b.log("switching audiotrack, live stream, unknown PTS,load first fragment"),
                                m = 0;
                            else if (m = t,
                            r.PTSKnown && t < D) {
                                if (!(h.end > D || h.nextStart))
                                    return;
                                p.b.log("alt audio track ahead of main track, seek to start of alt audio track"),
                                this.media.currentTime = D + .05
                            }
                        if (r.initSegment && !r.initSegment.data)
                            k = r.initSegment;
                        else if (m <= D) {
                            if (k = w[0],
                            null !== this.videoTrackCC && k.cc !== this.videoTrackCC && (k = Object(g.b)(w, this.videoTrackCC)),
                            r.live && k.loadIdx && k.loadIdx === this.fragLoadIdx) {
                                var O = h.nextStart ? h.nextStart : D;
                                return p.b.log("no alt audio available @currentTime:" + this.media.currentTime + ", seeking @" + (O + .05)),
                                void (this.media.currentTime = O + .05)
                            }
                        } else {
                            var C = void 0
                              , P = a.maxFragLookUpTolerance
                              , x = b ? w[b.sn - w[0].sn + 1] : void 0
                              , F = function(t) {
                                var e = Math.min(P, t.duration);
                                return t.start + t.duration - e <= m ? 1 : t.start - e > m && t.start ? -1 : 0
                            };
                            m < I ? (m > I - P && (P = 0),
                            C = x && !F(x) ? x : s.a.search(w, F)) : C = w[L - 1],
                            C && (k = C,
                            D = C.start,
                            b && k.level === b.level && k.sn === b.sn && (k.sn < r.endSN ? (k = w[k.sn + 1 - r.startSN],
                            p.b.log("SN just loaded, load next one: " + k.sn)) : k = null))
                        }
                        k && (k.encrypted ? (p.b.log("Loading key for " + k.sn + " of [" + r.startSN + " ," + r.endSN + "],track " + _),
                        this.state = S.KEY_LOADING,
                        i.trigger(d.a.KEY_LOADING, {
                            frag: k
                        })) : (p.b.log("Loading " + k.sn + ", cc: " + k.cc + " of [" + r.startSN + " ," + r.endSN + "],track " + _ + ", currentTime:" + t + ",bufferEnd:" + m.toFixed(3)),
                        (R || this.fragmentTracker.getState(k) === y.a.NOT_LOADED) && (this.fragCurrent = k,
                        this.startFragRequested = !0,
                        Object(o.a)(k.sn) && (this.nextLoadPosition = k.start + k.duration),
                        i.trigger(d.a.FRAG_LOADING, {
                            frag: k
                        }),
                        this.state = S.FRAG_LOADING)))
                    }
                    break;
                case S.WAITING_TRACK:
                    e = this.tracks[this.trackId],
                    e && e.details && (this.state = S.IDLE);
                    break;
                case S.FRAG_LOADING_WAITING_RETRY:
                    var M = T.now()
                      , N = this.retryDate;
                    u = this.media;
                    var U = u && u.seeking;
                    (!N || M >= N || U) && (p.b.log("audioStreamController: retryDate reached, switch back to IDLE state"),
                    this.state = S.IDLE);
                    break;
                case S.WAITING_INIT_PTS:
                    var B = this.videoTrackCC;
                    if (void 0 === this.initPTS[B])
                        break;
                    var G = this.waitingFragment;
                    if (G) {
                        var K = G.frag.cc;
                        B !== K ? (e = this.tracks[this.trackId],
                        e.details && e.details.live && (p.b.warn("Waiting fragment CC (" + K + ") does not match video track CC (" + B + ")"),
                        this.waitingFragment = null,
                        this.state = S.IDLE)) : (this.state = S.FRAG_LOADING,
                        this.onFragLoaded(this.waitingFragment),
                        this.waitingFragment = null)
                    } else
                        this.state = S.IDLE;
                    break;
                case S.STOPPED:
                case S.FRAG_LOADING:
                case S.PARSING:
                case S.PARSED:
                case S.ENDED:
                }
            }
            ,
            e.prototype.onMediaAttached = function(t) {
                var e = this.media = this.mediaBuffer = t.media;
                this.onvseeking = this.onMediaSeeking.bind(this),
                this.onvended = this.onMediaEnded.bind(this),
                e.addEventListener("seeking", this.onvseeking),
                e.addEventListener("ended", this.onvended);
                var r = this.config;
                this.tracks && r.autoStartLoad && this.startLoad(r.startPosition)
            }
            ,
            e.prototype.onMediaDetaching = function() {
                var t = this.media;
                t && t.ended && (p.b.log("MSE detaching and video ended, reset startPosition"),
                this.startPosition = this.lastCurrentTime = 0),
                t && (t.removeEventListener("seeking", this.onvseeking),
                t.removeEventListener("ended", this.onvended),
                this.onvseeking = this.onvseeked = this.onvended = null),
                this.media = this.mediaBuffer = this.videoBuffer = null,
                this.loadedmetadata = !1,
                this.stopLoad()
            }
            ,
            e.prototype.onMediaSeeking = function() {
                this.state === S.ENDED && (this.state = S.IDLE),
                this.media && (this.lastCurrentTime = this.media.currentTime),
                this.tick()
            }
            ,
            e.prototype.onMediaEnded = function() {
                this.startPosition = this.lastCurrentTime = 0
            }
            ,
            e.prototype.onAudioTracksUpdated = function(t) {
                p.b.log("audio tracks updated"),
                this.tracks = t.audioTracks
            }
            ,
            e.prototype.onAudioTrackSwitching = function(t) {
                var e = !!t.url;
                this.trackId = t.id,
                this.fragCurrent = null,
                this.state = S.PAUSED,
                this.waitingFragment = null,
                e ? this.setInterval(100) : this.demuxer && (this.demuxer.destroy(),
                this.demuxer = null),
                e && (this.audioSwitch = !0,
                this.state = S.IDLE),
                this.tick()
            }
            ,
            e.prototype.onAudioTrackLoaded = function(t) {
                var e = t.details
                  , r = t.id
                  , i = this.tracks[r]
                  , a = e.totalduration
                  , n = 0;
                if (p.b.log("track " + r + " loaded [" + e.startSN + "," + e.endSN + "],duration:" + a),
                e.live) {
                    var s = i.details;
                    s && e.fragments.length > 0 ? (c.b(s, e),
                    n = e.fragments[0].start,
                    e.PTSKnown ? p.b.log("live audio playlist sliding:" + n.toFixed(3)) : p.b.log("live audio playlist - outdated PTS, unknown sliding")) : (e.PTSKnown = !1,
                    p.b.log("live audio playlist - first load, unknown sliding"))
                } else
                    e.PTSKnown = !1;
                if (i.details = e,
                !this.startFragRequested) {
                    if (-1 === this.startPosition) {
                        var l = e.startTimeOffset;
                        Object(o.a)(l) ? (p.b.log("start time offset found in playlist, adjust startPosition to " + l),
                        this.startPosition = l) : this.startPosition = 0
                    }
                    this.nextLoadPosition = this.startPosition
                }
                this.state === S.WAITING_TRACK && (this.state = S.IDLE),
                this.tick()
            }
            ,
            e.prototype.onKeyLoaded = function() {
                this.state === S.KEY_LOADING && (this.state = S.IDLE,
                this.tick())
            }
            ,
            e.prototype.onFragLoaded = function(t) {
                var e = this.fragCurrent
                  , r = t.frag;
                if (this.state === S.FRAG_LOADING && e && "audio" === r.type && r.level === e.level && r.sn === e.sn) {
                    var i = this.tracks[this.trackId]
                      , a = i.details
                      , n = a.totalduration
                      , o = e.level
                      , s = e.sn
                      , l = e.cc
                      , c = this.config.defaultAudioCodec || i.audioCodec || "mp4a.40.2"
                      , h = this.stats = t.stats;
                    if ("initSegment" === s)
                        this.state = S.IDLE,
                        h.tparsed = h.tbuffered = T.now(),
                        a.initSegment.data = t.payload,
                        this.hls.trigger(d.a.FRAG_BUFFERED, {
                            stats: h,
                            frag: e,
                            id: "audio"
                        }),
                        this.tick();
                    else {
                        this.state = S.PARSING,
                        this.appended = !1,
                        this.demuxer || (this.demuxer = new u.a(this.hls,"audio"));
                        var f = this.initPTS[l]
                          , g = a.initSegment ? a.initSegment.data : [];
                        if (a.initSegment || void 0 !== f) {
                            this.pendingBuffering = !0,
                            p.b.log("Demuxing " + s + " of [" + a.startSN + " ," + a.endSN + "],track " + o);
                            this.demuxer.push(t.payload, g, c, null, e, n, !1, f)
                        } else
                            p.b.log("unknown video PTS for continuity counter " + l + ", waiting for video PTS before demuxing audio frag " + s + " of [" + a.startSN + " ," + a.endSN + "],track " + o),
                            this.waitingFragment = t,
                            this.state = S.WAITING_INIT_PTS
                    }
                }
                this.fragLoadError = 0
            }
            ,
            e.prototype.onFragParsingInitSegment = function(t) {
                var e = this.fragCurrent
                  , r = t.frag;
                if (e && "audio" === t.id && r.sn === e.sn && r.level === e.level && this.state === S.PARSING) {
                    var i = t.tracks
                      , a = void 0;
                    if (i.video && delete i.video,
                    a = i.audio) {
                        a.levelCodec = a.codec,
                        a.id = t.id,
                        this.hls.trigger(d.a.BUFFER_CODECS, i),
                        p.b.log("audio track:audio,container:" + a.container + ",codecs[level/parsed]=[" + a.levelCodec + "/" + a.codec + "]");
                        var n = a.initSegment;
                        if (n) {
                            var o = {
                                type: "audio",
                                data: n,
                                parent: "audio",
                                content: "initSegment"
                            };
                            this.audioSwitch ? this.pendingData = [o] : (this.appended = !0,
                            this.pendingBuffering = !0,
                            this.hls.trigger(d.a.BUFFER_APPENDING, o))
                        }
                        this.tick()
                    }
                }
            }
            ,
            e.prototype.onFragParsingData = function(t) {
                var e = this
                  , r = this.fragCurrent
                  , i = t.frag;
                if (r && "audio" === t.id && "audio" === t.type && i.sn === r.sn && i.level === r.level && this.state === S.PARSING) {
                    var a = this.trackId
                      , n = this.tracks[a]
                      , s = this.hls;
                    Object(o.a)(t.endPTS) || (t.endPTS = t.startPTS + r.duration,
                    t.endDTS = t.startDTS + r.duration),
                    r.addElementaryStream(m.a.ElementaryStreamTypes.AUDIO),
                    p.b.log("parsed " + t.type + ",PTS:[" + t.startPTS.toFixed(3) + "," + t.endPTS.toFixed(3) + "],DTS:[" + t.startDTS.toFixed(3) + "/" + t.endDTS.toFixed(3) + "],nb:" + t.nb),
                    c.c(n.details, r, t.startPTS, t.endPTS);
                    var l = this.audioSwitch
                      , u = this.media
                      , h = !1;
                    if (l && u)
                        if (u.readyState) {
                            var g = u.currentTime;
                            p.b.log("switching audio track : currentTime:" + g),
                            g >= t.startPTS && (p.b.log("switching audio track : flushing all audio"),
                            this.state = S.BUFFER_FLUSHING,
                            s.trigger(d.a.BUFFER_FLUSHING, {
                                startOffset: 0,
                                endOffset: Number.POSITIVE_INFINITY,
                                type: "audio"
                            }),
                            h = !0,
                            this.audioSwitch = !1,
                            s.trigger(d.a.AUDIO_TRACK_SWITCHED, {
                                id: a
                            }))
                        } else
                            this.audioSwitch = !1,
                            s.trigger(d.a.AUDIO_TRACK_SWITCHED, {
                                id: a
                            });
                    var v = this.pendingData;
                    if (!v)
                        return p.b.warn("Apparently attempt to enqueue media payload without codec initialization data upfront"),
                        void s.trigger(d.a.ERROR, {
                            type: f.b.MEDIA_ERROR,
                            details: null,
                            fatal: !0
                        });
                    this.audioSwitch || ([t.data1, t.data2].forEach(function(e) {
                        e && e.length && v.push({
                            type: t.type,
                            data: e,
                            parent: "audio",
                            content: "data"
                        })
                    }),
                    !h && v.length && (v.forEach(function(t) {
                        e.state === S.PARSING && (e.pendingBuffering = !0,
                        e.hls.trigger(d.a.BUFFER_APPENDING, t))
                    }),
                    this.pendingData = [],
                    this.appended = !0)),
                    this.tick()
                }
            }
            ,
            e.prototype.onFragParsed = function(t) {
                var e = this.fragCurrent
                  , r = t.frag;
                e && "audio" === t.id && r.sn === e.sn && r.level === e.level && this.state === S.PARSING && (this.stats.tparsed = T.now(),
                this.state = S.PARSED,
                this._checkAppendedParsed())
            }
            ,
            e.prototype.onBufferReset = function() {
                this.mediaBuffer = this.videoBuffer = null,
                this.loadedmetadata = !1
            }
            ,
            e.prototype.onBufferCreated = function(t) {
                var e = t.tracks.audio;
                e && (this.mediaBuffer = e.buffer,
                this.loadedmetadata = !0),
                t.tracks.video && (this.videoBuffer = t.tracks.video.buffer)
            }
            ,
            e.prototype.onBufferAppended = function(t) {
                if ("audio" === t.parent) {
                    var e = this.state;
                    e !== S.PARSING && e !== S.PARSED || (this.pendingBuffering = t.pending > 0,
                    this._checkAppendedParsed())
                }
            }
            ,
            e.prototype._checkAppendedParsed = function() {
                if (!(this.state !== S.PARSED || this.appended && this.pendingBuffering)) {
                    var t = this.fragCurrent
                      , e = this.stats
                      , r = this.hls;
                    if (t) {
                        this.fragPrevious = t,
                        e.tbuffered = T.now(),
                        r.trigger(d.a.FRAG_BUFFERED, {
                            stats: e,
                            frag: t,
                            id: "audio"
                        });
                        var i = this.mediaBuffer ? this.mediaBuffer : this.media;
                        p.b.log("audio buffered : " + h.a.toString(i.buffered)),
                        this.audioSwitch && this.appended && (this.audioSwitch = !1,
                        r.trigger(d.a.AUDIO_TRACK_SWITCHED, {
                            id: this.trackId
                        })),
                        this.state = S.IDLE
                    }
                    this.tick()
                }
            }
            ,
            e.prototype.onError = function(t) {
                var e = t.frag;
                if (!e || "audio" === e.type)
                    switch (t.details) {
                    case f.a.FRAG_LOAD_ERROR:
                    case f.a.FRAG_LOAD_TIMEOUT:
                        var r = t.frag;
                        if (r && "audio" !== r.type)
                            break;
                        if (!t.fatal) {
                            var i = this.fragLoadError;
                            i ? i++ : i = 1;
                            var a = this.config;
                            if (i <= a.fragLoadingMaxRetry) {
                                this.fragLoadError = i;
                                var n = Math.min(Math.pow(2, i - 1) * a.fragLoadingRetryDelay, a.fragLoadingMaxRetryTimeout);
                                p.b.warn("AudioStreamController: frag loading failed, retry in " + n + " ms"),
                                this.retryDate = T.now() + n,
                                this.state = S.FRAG_LOADING_WAITING_RETRY
                            } else
                                p.b.error("AudioStreamController: " + t.details + " reaches max retry, redispatch as fatal ..."),
                                t.fatal = !0,
                                this.state = S.ERROR
                        }
                        break;
                    case f.a.AUDIO_TRACK_LOAD_ERROR:
                    case f.a.AUDIO_TRACK_LOAD_TIMEOUT:
                    case f.a.KEY_LOAD_ERROR:
                    case f.a.KEY_LOAD_TIMEOUT:
                        this.state !== S.ERROR && (this.state = t.fatal ? S.ERROR : S.IDLE,
                        p.b.warn("AudioStreamController: " + t.details + " while loading frag, now switching to " + this.state + " state ..."));
                        break;
                    case f.a.BUFFER_FULL_ERROR:
                        if ("audio" === t.parent && (this.state === S.PARSING || this.state === S.PARSED)) {
                            var o = this.mediaBuffer
                              , s = this.media.currentTime;
                            if (o && l.a.isBuffered(o, s) && l.a.isBuffered(o, s + .5)) {
                                var u = this.config;
                                u.maxMaxBufferLength >= u.maxBufferLength && (u.maxMaxBufferLength /= 2,
                                p.b.warn("AudioStreamController: reduce max buffer length to " + u.maxMaxBufferLength + "s")),
                                this.state = S.IDLE
                            } else
                                p.b.warn("AudioStreamController: buffer full error also media.currentTime is not buffered, flush audio buffer"),
                                this.fragCurrent = null,
                                this.state = S.BUFFER_FLUSHING,
                                this.hls.trigger(d.a.BUFFER_FLUSHING, {
                                    startOffset: 0,
                                    endOffset: Number.POSITIVE_INFINITY,
                                    type: "audio"
                                })
                        }
                    }
            }
            ,
            e.prototype.onBufferFlushed = function() {
                var t = this
                  , e = this.pendingData;
                e && e.length ? (p.b.log("AudioStreamController: appending pending audio data after buffer flushed"),
                e.forEach(function(e) {
                    t.hls.trigger(d.a.BUFFER_APPENDING, e)
                }),
                this.appended = !0,
                this.pendingData = [],
                this.state = S.PARSED) : (this.state = S.IDLE,
                this.fragPrevious = null,
                this.tick())
            }
            ,
            b(e, [{
                key: "state",
                set: function(t) {
                    if (this.state !== t) {
                        var e = this.state;
                        this._state = t,
                        p.b.log("audio stream:" + e + "->" + t)
                    }
                },
                get: function() {
                    return this._state
                }
            }]),
            e
        }(v.a);
        e.a = A
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e, r, i) {
            for (var n = void 0, o = void 0, s = void 0, l = void 0, u = void 0, d = window.VTTCue || window.TextTrackCue, c = 0; c < i.rows.length; c++)
                if (n = i.rows[c],
                s = !0,
                l = 0,
                u = "",
                !n.isEmpty()) {
                    for (var h = 0; h < n.chars.length; h++)
                        n.chars[h].uchar.match(/\s/) && s ? l++ : (u += n.chars[h].uchar,
                        s = !1);
                    n.cueStartTime = e,
                    e === r && (r += 1e-4),
                    o = new d(e,r,Object(a.b)(u.trim())),
                    l >= 16 ? l-- : l++,
                    navigator.userAgent.match(/Firefox\//) ? o.line = c + 1 : o.line = c > 7 ? c - 2 : c + 1,
                    o.align = "left",
                    o.position = Math.max(0, Math.min(100, l / 32 * 100 + (navigator.userAgent.match(/Firefox\//) ? 50 : 0))),
                    t.addCue(o)
                }
        }
        Object.defineProperty(e, "__esModule", {
            value: !0
        }),
        e.newCue = i;
        var a = r(28)
    }
    , function(t, e, r) {
        "use strict";
        e.a = function() {
            function t(t) {
                return "string" == typeof t && (!!n[t.toLowerCase()] && t.toLowerCase())
            }
            function e(t) {
                return "string" == typeof t && (!!o[t.toLowerCase()] && t.toLowerCase())
            }
            function r(t) {
                for (var e = 1; e < arguments.length; e++) {
                    var r = arguments[e];
                    for (var i in r)
                        t[i] = r[i]
                }
                return t
            }
            function i(i, n, o) {
                var s = this
                  , l = function() {
                    if ("undefined" != typeof navigator)
                        return /MSIE\s8\.0/.test(navigator.userAgent)
                }()
                  , u = {};
                l ? s = document.createElement("custom") : u.enumerable = !0,
                s.hasBeenReset = !1;
                var d = ""
                  , c = !1
                  , h = i
                  , f = n
                  , p = o
                  , g = null
                  , v = ""
                  , y = !0
                  , m = "auto"
                  , b = "start"
                  , E = 50
                  , T = "middle"
                  , S = 50
                  , A = "middle";
                if (Object.defineProperty(s, "id", r({}, u, {
                    get: function() {
                        return d
                    },
                    set: function(t) {
                        d = "" + t
                    }
                })),
                Object.defineProperty(s, "pauseOnExit", r({}, u, {
                    get: function() {
                        return c
                    },
                    set: function(t) {
                        c = !!t
                    }
                })),
                Object.defineProperty(s, "startTime", r({}, u, {
                    get: function() {
                        return h
                    },
                    set: function(t) {
                        if ("number" != typeof t)
                            throw new TypeError("Start time must be set to a number.");
                        h = t,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "endTime", r({}, u, {
                    get: function() {
                        return f
                    },
                    set: function(t) {
                        if ("number" != typeof t)
                            throw new TypeError("End time must be set to a number.");
                        f = t,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "text", r({}, u, {
                    get: function() {
                        return p
                    },
                    set: function(t) {
                        p = "" + t,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "region", r({}, u, {
                    get: function() {
                        return g
                    },
                    set: function(t) {
                        g = t,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "vertical", r({}, u, {
                    get: function() {
                        return v
                    },
                    set: function(e) {
                        var r = t(e);
                        if (!1 === r)
                            throw new SyntaxError("An invalid or illegal string was specified.");
                        v = r,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "snapToLines", r({}, u, {
                    get: function() {
                        return y
                    },
                    set: function(t) {
                        y = !!t,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "line", r({}, u, {
                    get: function() {
                        return m
                    },
                    set: function(t) {
                        if ("number" != typeof t && t !== a)
                            throw new SyntaxError("An invalid number or illegal string was specified.");
                        m = t,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "lineAlign", r({}, u, {
                    get: function() {
                        return b
                    },
                    set: function(t) {
                        var r = e(t);
                        if (!r)
                            throw new SyntaxError("An invalid or illegal string was specified.");
                        b = r,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "position", r({}, u, {
                    get: function() {
                        return E
                    },
                    set: function(t) {
                        if (t < 0 || t > 100)
                            throw new Error("Position must be between 0 and 100.");
                        E = t,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "positionAlign", r({}, u, {
                    get: function() {
                        return T
                    },
                    set: function(t) {
                        var r = e(t);
                        if (!r)
                            throw new SyntaxError("An invalid or illegal string was specified.");
                        T = r,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "size", r({}, u, {
                    get: function() {
                        return S
                    },
                    set: function(t) {
                        if (t < 0 || t > 100)
                            throw new Error("Size must be between 0 and 100.");
                        S = t,
                        this.hasBeenReset = !0
                    }
                })),
                Object.defineProperty(s, "align", r({}, u, {
                    get: function() {
                        return A
                    },
                    set: function(t) {
                        var r = e(t);
                        if (!r)
                            throw new SyntaxError("An invalid or illegal string was specified.");
                        A = r,
                        this.hasBeenReset = !0
                    }
                })),
                s.displayState = void 0,
                l)
                    return s
            }
            if ("undefined" != typeof window && window.VTTCue)
                return window.VTTCue;
            var a = "auto"
              , n = {
                "": !0,
                lr: !0,
                rl: !0
            }
              , o = {
                start: !0,
                middle: !0,
                end: !0,
                left: !0,
                right: !0
            };
            return i.prototype.getCueAsHTML = function() {
                return window.WebVTT.convertCueToDOMTree(window, this.text)
            }
            ,
            i
        }()
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        function o(t, e) {
            return t && t.label === e.name && !(t.textTrack1 || t.textTrack2)
        }
        function s(t, e, r, i) {
            return Math.min(e, i) - Math.max(t, r)
        }
        var l = r(1)
          , u = r(4)
          , d = r(68)
          , c = r(69)
          , h = r(70)
          , f = r(0)
          , p = r(27)
          , g = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, l.a.MEDIA_ATTACHING, l.a.MEDIA_DETACHING, l.a.FRAG_PARSING_USERDATA, l.a.FRAG_DECRYPTED, l.a.MANIFEST_LOADING, l.a.MANIFEST_LOADED, l.a.FRAG_LOADED, l.a.LEVEL_SWITCHING, l.a.INIT_PTS_FOUND));
                if (n.hls = r,
                n.config = r.config,
                n.enabled = !0,
                n.Cues = r.config.cueHandler,
                n.textTracks = [],
                n.tracks = [],
                n.unparsedVttFrags = [],
                n.initPTS = void 0,
                n.cueRanges = [],
                n.captionsTracks = {},
                n.captionsProperties = {
                    textTrack1: {
                        label: n.config.captionsTextTrack1Label,
                        languageCode: n.config.captionsTextTrack1LanguageCode
                    },
                    textTrack2: {
                        label: n.config.captionsTextTrack2Label,
                        languageCode: n.config.captionsTextTrack2LanguageCode
                    }
                },
                n.config.enableCEA708Captions) {
                    var o = new c.a(n,"textTrack1")
                      , s = new c.a(n,"textTrack2");
                    n.cea608Parser = new d.a(0,o,s)
                }
                return n
            }
            return n(e, t),
            e.prototype.addCues = function(t, e, r, i) {
                for (var a = this.cueRanges, n = !1, o = a.length; o--; ) {
                    var l = a[o]
                      , u = s(l[0], l[1], e, r);
                    if (u >= 0 && (l[0] = Math.min(l[0], e),
                    l[1] = Math.max(l[1], r),
                    n = !0,
                    u / (r - e) > .5))
                        return
                }
                n || a.push([e, r]),
                this.Cues.newCue(this.captionsTracks[t], e, r, i)
            }
            ,
            e.prototype.onInitPtsFound = function(t) {
                var e = this;
                void 0 === this.initPTS && (this.initPTS = t.initPTS),
                this.unparsedVttFrags.length && (this.unparsedVttFrags.forEach(function(t) {
                    e.onFragLoaded(t)
                }),
                this.unparsedVttFrags = [])
            }
            ,
            e.prototype.getExistingTrack = function(t) {
                var e = this.media;
                if (e)
                    for (var r = 0; r < e.textTracks.length; r++) {
                        var i = e.textTracks[r];
                        if (i[t])
                            return i
                    }
                return null
            }
            ,
            e.prototype.createCaptionsTrack = function(t) {
                var e = this.captionsProperties[t]
                  , r = e.label
                  , i = e.languageCode
                  , a = this.captionsTracks;
                if (!a[t]) {
                    var n = this.getExistingTrack(t);
                    if (n)
                        a[t] = n,
                        Object(p.a)(a[t]),
                        Object(p.b)(a[t], this.media);
                    else {
                        var o = this.createTextTrack("captions", r, i);
                        o && (o[t] = !0,
                        a[t] = o)
                    }
                }
            }
            ,
            e.prototype.createTextTrack = function(t, e, r) {
                var i = this.media;
                if (i)
                    return i.addTextTrack(t, e, r)
            }
            ,
            e.prototype.destroy = function() {
                u.a.prototype.destroy.call(this)
            }
            ,
            e.prototype.onMediaAttaching = function(t) {
                this.media = t.media,
                this._cleanTracks()
            }
            ,
            e.prototype.onMediaDetaching = function() {
                var t = this.captionsTracks;
                Object.keys(t).forEach(function(e) {
                    Object(p.a)(t[e]),
                    delete t[e]
                })
            }
            ,
            e.prototype.onManifestLoading = function() {
                this.lastSn = -1,
                this.prevCC = -1,
                this.vttCCs = {
                    ccOffset: 0,
                    presentationOffset: 0
                },
                this._cleanTracks()
            }
            ,
            e.prototype._cleanTracks = function() {
                var t = this.media;
                if (t) {
                    var e = t.textTracks;
                    if (e)
                        for (var r = 0; r < e.length; r++)
                            Object(p.a)(e[r])
                }
            }
            ,
            e.prototype.onManifestLoaded = function(t) {
                var e = this;
                if (this.textTracks = [],
                this.unparsedVttFrags = this.unparsedVttFrags || [],
                this.initPTS = void 0,
                this.cueRanges = [],
                this.config.enableWebVTT) {
                    this.tracks = t.subtitles || [];
                    var r = this.media ? this.media.textTracks : [];
                    this.tracks.forEach(function(t, i) {
                        var a = void 0;
                        if (i < r.length) {
                            var n = r[i];
                            o(n, t) && (a = n)
                        }
                        a || (a = e.createTextTrack("subtitles", t.name, t.lang)),
                        t.default ? a.mode = e.hls.subtitleDisplay ? "showing" : "hidden" : a.mode = "disabled",
                        e.textTracks.push(a)
                    })
                }
            }
            ,
            e.prototype.onLevelSwitching = function() {
                this.enabled = "NONE" !== this.hls.currentLevel.closedCaptions
            }
            ,
            e.prototype.onFragLoaded = function(t) {
                var e = t.frag
                  , r = t.payload;
                if ("main" === e.type) {
                    var i = e.sn;
                    if (i !== this.lastSn + 1) {
                        var a = this.cea608Parser;
                        a && a.reset()
                    }
                    this.lastSn = i
                } else if ("subtitle" === e.type)
                    if (r.byteLength) {
                        if (void 0 === this.initPTS)
                            return void this.unparsedVttFrags.push(t);
                        var n = e.decryptdata;
                        null != n && null != n.key && "AES-128" === n.method || this._parseVTTs(e, r)
                    } else
                        this.hls.trigger(l.a.SUBTITLE_FRAG_PROCESSED, {
                            success: !1,
                            frag: e
                        })
            }
            ,
            e.prototype._parseVTTs = function(t, e) {
                var r = this.vttCCs;
                r[t.cc] || (r[t.cc] = {
                    start: t.start,
                    prevCC: this.prevCC,
                    new: !0
                },
                this.prevCC = t.cc);
                var i = this.textTracks
                  , a = this.hls;
                h.a.parse(e, this.initPTS, r, t.cc, function(e) {
                    var r = i[t.trackId];
                    if ("disabled" === r.mode)
                        return void a.trigger(l.a.SUBTITLE_FRAG_PROCESSED, {
                            success: !1,
                            frag: t
                        });
                    e.forEach(function(t) {
                        if (!r.cues.getCueById(t.id))
                            try {
                                r.addCue(t)
                            } catch (i) {
                                var e = new window.TextTrackCue(t.startTime,t.endTime,t.text);
                                e.id = t.id,
                                r.addCue(e)
                            }
                    }),
                    a.trigger(l.a.SUBTITLE_FRAG_PROCESSED, {
                        success: !0,
                        frag: t
                    })
                }, function(e) {
                    f.b.log("Failed to parse VTT cue: " + e),
                    a.trigger(l.a.SUBTITLE_FRAG_PROCESSED, {
                        success: !1,
                        frag: t
                    })
                })
            }
            ,
            e.prototype.onFragDecrypted = function(t) {
                var e = t.payload
                  , r = t.frag;
                if ("subtitle" === r.type) {
                    if (void 0 === this.initPTS)
                        return void this.unparsedVttFrags.push(t);
                    this._parseVTTs(r, e)
                }
            }
            ,
            e.prototype.onFragParsingUserdata = function(t) {
                if (this.enabled && this.config.enableCEA708Captions)
                    for (var e = 0; e < t.samples.length; e++) {
                        var r = this.extractCea608Data(t.samples[e].bytes);
                        this.cea608Parser.addData(t.samples[e].pts, r)
                    }
            }
            ,
            e.prototype.extractCea608Data = function(t) {
                for (var e = 31 & t[0], r = 2, i = void 0, a = void 0, n = void 0, o = void 0, s = void 0, l = [], u = 0; u < e; u++)
                    i = t[r++],
                    a = 127 & t[r++],
                    n = 127 & t[r++],
                    o = 0 != (4 & i),
                    s = 3 & i,
                    0 === a && 0 === n || o && 0 === s && (l.push(a),
                    l.push(n));
                return l
            }
            ,
            e
        }(u.a);
        e.a = g
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = {
            42: 225,
            92: 233,
            94: 237,
            95: 243,
            96: 250,
            123: 231,
            124: 247,
            125: 209,
            126: 241,
            127: 9608,
            128: 174,
            129: 176,
            130: 189,
            131: 191,
            132: 8482,
            133: 162,
            134: 163,
            135: 9834,
            136: 224,
            137: 32,
            138: 232,
            139: 226,
            140: 234,
            141: 238,
            142: 244,
            143: 251,
            144: 193,
            145: 201,
            146: 211,
            147: 218,
            148: 220,
            149: 252,
            150: 8216,
            151: 161,
            152: 42,
            153: 8217,
            154: 9473,
            155: 169,
            156: 8480,
            157: 8226,
            158: 8220,
            159: 8221,
            160: 192,
            161: 194,
            162: 199,
            163: 200,
            164: 202,
            165: 203,
            166: 235,
            167: 206,
            168: 207,
            169: 239,
            170: 212,
            171: 217,
            172: 249,
            173: 219,
            174: 171,
            175: 187,
            176: 195,
            177: 227,
            178: 205,
            179: 204,
            180: 236,
            181: 210,
            182: 242,
            183: 213,
            184: 245,
            185: 123,
            186: 125,
            187: 92,
            188: 94,
            189: 95,
            190: 124,
            191: 8764,
            192: 196,
            193: 228,
            194: 214,
            195: 246,
            196: 223,
            197: 165,
            198: 164,
            199: 9475,
            200: 197,
            201: 229,
            202: 216,
            203: 248,
            204: 9487,
            205: 9491,
            206: 9495,
            207: 9499
        }
          , n = function(t) {
            var e = t;
            return a.hasOwnProperty(t) && (e = a[t]),
            String.fromCharCode(e)
        }
          , o = 15
          , s = 100
          , l = {
            17: 1,
            18: 3,
            21: 5,
            22: 7,
            23: 9,
            16: 11,
            19: 12,
            20: 14
        }
          , u = {
            17: 2,
            18: 4,
            21: 6,
            22: 8,
            23: 10,
            19: 13,
            20: 15
        }
          , d = {
            25: 1,
            26: 3,
            29: 5,
            30: 7,
            31: 9,
            24: 11,
            27: 12,
            28: 14
        }
          , c = {
            25: 2,
            26: 4,
            29: 6,
            30: 8,
            31: 10,
            27: 13,
            28: 15
        }
          , h = ["white", "green", "blue", "cyan", "red", "yellow", "magenta", "black", "transparent"]
          , f = {
            verboseFilter: {
                DATA: 3,
                DEBUG: 3,
                INFO: 2,
                WARNING: 2,
                TEXT: 1,
                ERROR: 0
            },
            time: null,
            verboseLevel: 0,
            setTime: function(t) {
                this.time = t
            },
            log: function(t, e) {
                this.verboseFilter[t];
                this.verboseLevel
            }
        }
          , p = function(t) {
            for (var e = [], r = 0; r < t.length; r++)
                e.push(t[r].toString(16));
            return e
        }
          , g = function() {
            function t(e, r, a, n, o) {
                i(this, t),
                this.foreground = e || "white",
                this.underline = r || !1,
                this.italics = a || !1,
                this.background = n || "black",
                this.flash = o || !1
            }
            return t.prototype.reset = function() {
                this.foreground = "white",
                this.underline = !1,
                this.italics = !1,
                this.background = "black",
                this.flash = !1
            }
            ,
            t.prototype.setStyles = function(t) {
                for (var e = ["foreground", "underline", "italics", "background", "flash"], r = 0; r < e.length; r++) {
                    var i = e[r];
                    t.hasOwnProperty(i) && (this[i] = t[i])
                }
            }
            ,
            t.prototype.isDefault = function() {
                return "white" === this.foreground && !this.underline && !this.italics && "black" === this.background && !this.flash
            }
            ,
            t.prototype.equals = function(t) {
                return this.foreground === t.foreground && this.underline === t.underline && this.italics === t.italics && this.background === t.background && this.flash === t.flash
            }
            ,
            t.prototype.copy = function(t) {
                this.foreground = t.foreground,
                this.underline = t.underline,
                this.italics = t.italics,
                this.background = t.background,
                this.flash = t.flash
            }
            ,
            t.prototype.toString = function() {
                return "color=" + this.foreground + ", underline=" + this.underline + ", italics=" + this.italics + ", background=" + this.background + ", flash=" + this.flash
            }
            ,
            t
        }()
          , v = function() {
            function t(e, r, a, n, o, s) {
                i(this, t),
                this.uchar = e || " ",
                this.penState = new g(r,a,n,o,s)
            }
            return t.prototype.reset = function() {
                this.uchar = " ",
                this.penState.reset()
            }
            ,
            t.prototype.setChar = function(t, e) {
                this.uchar = t,
                this.penState.copy(e)
            }
            ,
            t.prototype.setPenState = function(t) {
                this.penState.copy(t)
            }
            ,
            t.prototype.equals = function(t) {
                return this.uchar === t.uchar && this.penState.equals(t.penState)
            }
            ,
            t.prototype.copy = function(t) {
                this.uchar = t.uchar,
                this.penState.copy(t.penState)
            }
            ,
            t.prototype.isEmpty = function() {
                return " " === this.uchar && this.penState.isDefault()
            }
            ,
            t
        }()
          , y = function() {
            function t() {
                i(this, t),
                this.chars = [];
                for (var e = 0; e < s; e++)
                    this.chars.push(new v);
                this.pos = 0,
                this.currPenState = new g
            }
            return t.prototype.equals = function(t) {
                for (var e = !0, r = 0; r < s; r++)
                    if (!this.chars[r].equals(t.chars[r])) {
                        e = !1;
                        break
                    }
                return e
            }
            ,
            t.prototype.copy = function(t) {
                for (var e = 0; e < s; e++)
                    this.chars[e].copy(t.chars[e])
            }
            ,
            t.prototype.isEmpty = function() {
                for (var t = !0, e = 0; e < s; e++)
                    if (!this.chars[e].isEmpty()) {
                        t = !1;
                        break
                    }
                return t
            }
            ,
            t.prototype.setCursor = function(t) {
                this.pos !== t && (this.pos = t),
                this.pos < 0 ? (f.log("ERROR", "Negative cursor position " + this.pos),
                this.pos = 0) : this.pos > s && (f.log("ERROR", "Too large cursor position " + this.pos),
                this.pos = s)
            }
            ,
            t.prototype.moveCursor = function(t) {
                var e = this.pos + t;
                if (t > 1)
                    for (var r = this.pos + 1; r < e + 1; r++)
                        this.chars[r].setPenState(this.currPenState);
                this.setCursor(e)
            }
            ,
            t.prototype.backSpace = function() {
                this.moveCursor(-1),
                this.chars[this.pos].setChar(" ", this.currPenState)
            }
            ,
            t.prototype.insertChar = function(t) {
                t >= 144 && this.backSpace();
                var e = n(t);
                if (this.pos >= s)
                    return void f.log("ERROR", "Cannot insert " + t.toString(16) + " (" + e + ") at position " + this.pos + ". Skipping it!");
                this.chars[this.pos].setChar(e, this.currPenState),
                this.moveCursor(1)
            }
            ,
            t.prototype.clearFromPos = function(t) {
                var e = void 0;
                for (e = t; e < s; e++)
                    this.chars[e].reset()
            }
            ,
            t.prototype.clear = function() {
                this.clearFromPos(0),
                this.pos = 0,
                this.currPenState.reset()
            }
            ,
            t.prototype.clearToEndOfRow = function() {
                this.clearFromPos(this.pos)
            }
            ,
            t.prototype.getTextString = function() {
                for (var t = [], e = !0, r = 0; r < s; r++) {
                    var i = this.chars[r].uchar;
                    " " !== i && (e = !1),
                    t.push(i)
                }
                return e ? "" : t.join("")
            }
            ,
            t.prototype.setPenStyles = function(t) {
                this.currPenState.setStyles(t),
                this.chars[this.pos].setPenState(this.currPenState)
            }
            ,
            t
        }()
          , m = function() {
            function t() {
                i(this, t),
                this.rows = [];
                for (var e = 0; e < o; e++)
                    this.rows.push(new y);
                this.currRow = o - 1,
                this.nrRollUpRows = null,
                this.reset()
            }
            return t.prototype.reset = function() {
                for (var t = 0; t < o; t++)
                    this.rows[t].clear();
                this.currRow = o - 1
            }
            ,
            t.prototype.equals = function(t) {
                for (var e = !0, r = 0; r < o; r++)
                    if (!this.rows[r].equals(t.rows[r])) {
                        e = !1;
                        break
                    }
                return e
            }
            ,
            t.prototype.copy = function(t) {
                for (var e = 0; e < o; e++)
                    this.rows[e].copy(t.rows[e])
            }
            ,
            t.prototype.isEmpty = function() {
                for (var t = !0, e = 0; e < o; e++)
                    if (!this.rows[e].isEmpty()) {
                        t = !1;
                        break
                    }
                return t
            }
            ,
            t.prototype.backSpace = function() {
                this.rows[this.currRow].backSpace()
            }
            ,
            t.prototype.clearToEndOfRow = function() {
                this.rows[this.currRow].clearToEndOfRow()
            }
            ,
            t.prototype.insertChar = function(t) {
                this.rows[this.currRow].insertChar(t)
            }
            ,
            t.prototype.setPen = function(t) {
                this.rows[this.currRow].setPenStyles(t)
            }
            ,
            t.prototype.moveCursor = function(t) {
                this.rows[this.currRow].moveCursor(t)
            }
            ,
            t.prototype.setCursor = function(t) {
                f.log("INFO", "setCursor: " + t),
                this.rows[this.currRow].setCursor(t)
            }
            ,
            t.prototype.setPAC = function(t) {
                f.log("INFO", "pacData = " + JSON.stringify(t));
                var e = t.row - 1;
                if (this.nrRollUpRows && e < this.nrRollUpRows - 1 && (e = this.nrRollUpRows - 1),
                this.nrRollUpRows && this.currRow !== e) {
                    for (var r = 0; r < o; r++)
                        this.rows[r].clear();
                    var i = this.currRow + 1 - this.nrRollUpRows
                      , a = this.lastOutputScreen;
                    if (a) {
                        var n = a.rows[i].cueStartTime;
                        if (n && n < f.time)
                            for (var s = 0; s < this.nrRollUpRows; s++)
                                this.rows[e - this.nrRollUpRows + s + 1].copy(a.rows[i + s])
                    }
                }
                this.currRow = e;
                var l = this.rows[this.currRow];
                if (null !== t.indent) {
                    var u = t.indent
                      , d = Math.max(u - 1, 0);
                    l.setCursor(t.indent),
                    t.color = l.chars[d].penState.foreground
                }
                var c = {
                    foreground: t.color,
                    underline: t.underline,
                    italics: t.italics,
                    background: "black",
                    flash: !1
                };
                this.setPen(c)
            }
            ,
            t.prototype.setBkgData = function(t) {
                f.log("INFO", "bkgData = " + JSON.stringify(t)),
                this.backSpace(),
                this.setPen(t),
                this.insertChar(32)
            }
            ,
            t.prototype.setRollUpRows = function(t) {
                this.nrRollUpRows = t
            }
            ,
            t.prototype.rollUp = function() {
                if (null === this.nrRollUpRows)
                    return void f.log("DEBUG", "roll_up but nrRollUpRows not set yet");
                f.log("TEXT", this.getDisplayText());
                var t = this.currRow + 1 - this.nrRollUpRows
                  , e = this.rows.splice(t, 1)[0];
                e.clear(),
                this.rows.splice(this.currRow, 0, e),
                f.log("INFO", "Rolling up")
            }
            ,
            t.prototype.getDisplayText = function(t) {
                t = t || !1;
                for (var e = [], r = "", i = -1, a = 0; a < o; a++) {
                    var n = this.rows[a].getTextString();
                    n && (i = a + 1,
                    t ? e.push("Row " + i + ": '" + n + "'") : e.push(n.trim()))
                }
                return e.length > 0 && (r = t ? "[" + e.join(" | ") + "]" : e.join("\n")),
                r
            }
            ,
            t.prototype.getTextAndFormat = function() {
                return this.rows
            }
            ,
            t
        }()
          , b = function() {
            function t(e, r) {
                i(this, t),
                this.chNr = e,
                this.outputFilter = r,
                this.mode = null,
                this.verbose = 0,
                this.displayedMemory = new m,
                this.nonDisplayedMemory = new m,
                this.lastOutputScreen = new m,
                this.currRollUpRow = this.displayedMemory.rows[o - 1],
                this.writeScreen = this.displayedMemory,
                this.mode = null,
                this.cueStartTime = null
            }
            return t.prototype.reset = function() {
                this.mode = null,
                this.displayedMemory.reset(),
                this.nonDisplayedMemory.reset(),
                this.lastOutputScreen.reset(),
                this.currRollUpRow = this.displayedMemory.rows[o - 1],
                this.writeScreen = this.displayedMemory,
                this.mode = null,
                this.cueStartTime = null,
                this.lastCueEndTime = null
            }
            ,
            t.prototype.getHandler = function() {
                return this.outputFilter
            }
            ,
            t.prototype.setHandler = function(t) {
                this.outputFilter = t
            }
            ,
            t.prototype.setPAC = function(t) {
                this.writeScreen.setPAC(t)
            }
            ,
            t.prototype.setBkgData = function(t) {
                this.writeScreen.setBkgData(t)
            }
            ,
            t.prototype.setMode = function(t) {
                t !== this.mode && (this.mode = t,
                f.log("INFO", "MODE=" + t),
                "MODE_POP-ON" === this.mode ? this.writeScreen = this.nonDisplayedMemory : (this.writeScreen = this.displayedMemory,
                this.writeScreen.reset()),
                "MODE_ROLL-UP" !== this.mode && (this.displayedMemory.nrRollUpRows = null,
                this.nonDisplayedMemory.nrRollUpRows = null),
                this.mode = t)
            }
            ,
            t.prototype.insertChars = function(t) {
                for (var e = 0; e < t.length; e++)
                    this.writeScreen.insertChar(t[e]);
                var r = this.writeScreen === this.displayedMemory ? "DISP" : "NON_DISP";
                f.log("INFO", r + ": " + this.writeScreen.getDisplayText(!0)),
                "MODE_PAINT-ON" !== this.mode && "MODE_ROLL-UP" !== this.mode || (f.log("TEXT", "DISPLAYED: " + this.displayedMemory.getDisplayText(!0)),
                this.outputDataUpdate())
            }
            ,
            t.prototype.ccRCL = function() {
                f.log("INFO", "RCL - Resume Caption Loading"),
                this.setMode("MODE_POP-ON")
            }
            ,
            t.prototype.ccBS = function() {
                f.log("INFO", "BS - BackSpace"),
                "MODE_TEXT" !== this.mode && (this.writeScreen.backSpace(),
                this.writeScreen === this.displayedMemory && this.outputDataUpdate())
            }
            ,
            t.prototype.ccAOF = function() {}
            ,
            t.prototype.ccAON = function() {}
            ,
            t.prototype.ccDER = function() {
                f.log("INFO", "DER- Delete to End of Row"),
                this.writeScreen.clearToEndOfRow(),
                this.outputDataUpdate()
            }
            ,
            t.prototype.ccRU = function(t) {
                f.log("INFO", "RU(" + t + ") - Roll Up"),
                this.writeScreen = this.displayedMemory,
                this.setMode("MODE_ROLL-UP"),
                this.writeScreen.setRollUpRows(t)
            }
            ,
            t.prototype.ccFON = function() {
                f.log("INFO", "FON - Flash On"),
                this.writeScreen.setPen({
                    flash: !0
                })
            }
            ,
            t.prototype.ccRDC = function() {
                f.log("INFO", "RDC - Resume Direct Captioning"),
                this.setMode("MODE_PAINT-ON")
            }
            ,
            t.prototype.ccTR = function() {
                f.log("INFO", "TR"),
                this.setMode("MODE_TEXT")
            }
            ,
            t.prototype.ccRTD = function() {
                f.log("INFO", "RTD"),
                this.setMode("MODE_TEXT")
            }
            ,
            t.prototype.ccEDM = function() {
                f.log("INFO", "EDM - Erase Displayed Memory"),
                this.displayedMemory.reset(),
                this.outputDataUpdate(!0)
            }
            ,
            t.prototype.ccCR = function() {
                f.log("CR - Carriage Return"),
                this.writeScreen.rollUp(),
                this.outputDataUpdate(!0)
            }
            ,
            t.prototype.ccENM = function() {
                f.log("INFO", "ENM - Erase Non-displayed Memory"),
                this.nonDisplayedMemory.reset()
            }
            ,
            t.prototype.ccEOC = function() {
                if (f.log("INFO", "EOC - End Of Caption"),
                "MODE_POP-ON" === this.mode) {
                    var t = this.displayedMemory;
                    this.displayedMemory = this.nonDisplayedMemory,
                    this.nonDisplayedMemory = t,
                    this.writeScreen = this.nonDisplayedMemory,
                    f.log("TEXT", "DISP: " + this.displayedMemory.getDisplayText())
                }
                this.outputDataUpdate(!0)
            }
            ,
            t.prototype.ccTO = function(t) {
                f.log("INFO", "TO(" + t + ") - Tab Offset"),
                this.writeScreen.moveCursor(t)
            }
            ,
            t.prototype.ccMIDROW = function(t) {
                var e = {
                    flash: !1
                };
                if (e.underline = t % 2 == 1,
                e.italics = t >= 46,
                e.italics)
                    e.foreground = "white";
                else {
                    var r = Math.floor(t / 2) - 16
                      , i = ["white", "green", "blue", "cyan", "red", "yellow", "magenta"];
                    e.foreground = i[r]
                }
                f.log("INFO", "MIDROW: " + JSON.stringify(e)),
                this.writeScreen.setPen(e)
            }
            ,
            t.prototype.outputDataUpdate = function() {
                var t = arguments.length > 0 && void 0 !== arguments[0] && arguments[0]
                  , e = f.time;
                null !== e && this.outputFilter && (null !== this.cueStartTime || this.displayedMemory.isEmpty() ? this.displayedMemory.equals(this.lastOutputScreen) || (this.outputFilter.newCue && (this.outputFilter.newCue(this.cueStartTime, e, this.lastOutputScreen),
                !0 === t && this.outputFilter.dispatchCue && this.outputFilter.dispatchCue()),
                this.cueStartTime = this.displayedMemory.isEmpty() ? null : e) : this.cueStartTime = e,
                this.lastOutputScreen.copy(this.displayedMemory))
            }
            ,
            t.prototype.cueSplitAtTime = function(t) {
                this.outputFilter && (this.displayedMemory.isEmpty() || (this.outputFilter.newCue && this.outputFilter.newCue(this.cueStartTime, t, this.displayedMemory),
                this.cueStartTime = t))
            }
            ,
            t
        }()
          , E = function() {
            function t(e, r, a) {
                i(this, t),
                this.field = e || 1,
                this.outputs = [r, a],
                this.channels = [new b(1,r), new b(2,a)],
                this.currChNr = -1,
                this.lastCmdA = null,
                this.lastCmdB = null,
                this.bufferedData = [],
                this.startTime = null,
                this.lastTime = null,
                this.dataCounters = {
                    padding: 0,
                    char: 0,
                    cmd: 0,
                    other: 0
                }
            }
            return t.prototype.getHandler = function(t) {
                return this.channels[t].getHandler()
            }
            ,
            t.prototype.setHandler = function(t, e) {
                this.channels[t].setHandler(e)
            }
            ,
            t.prototype.addData = function(t, e) {
                var r = void 0
                  , i = void 0
                  , a = void 0
                  , n = !1;
                this.lastTime = t,
                f.setTime(t);
                for (var o = 0; o < e.length; o += 2)
                    if (i = 127 & e[o],
                    a = 127 & e[o + 1],
                    0 !== i || 0 !== a) {
                        if (f.log("DATA", "[" + p([e[o], e[o + 1]]) + "] -> (" + p([i, a]) + ")"),
                        r = this.parseCmd(i, a),
                        r || (r = this.parseMidrow(i, a)),
                        r || (r = this.parsePAC(i, a)),
                        r || (r = this.parseBackgroundAttributes(i, a)),
                        !r && (n = this.parseChars(i, a)))
                            if (this.currChNr && this.currChNr >= 0) {
                                var s = this.channels[this.currChNr - 1];
                                s.insertChars(n)
                            } else
                                f.log("WARNING", "No channel found yet. TEXT-MODE?");
                        r ? this.dataCounters.cmd += 2 : n ? this.dataCounters.char += 2 : (this.dataCounters.other += 2,
                        f.log("WARNING", "Couldn't parse cleaned data " + p([i, a]) + " orig: " + p([e[o], e[o + 1]])))
                    } else
                        this.dataCounters.padding += 2
            }
            ,
            t.prototype.parseCmd = function(t, e) {
                var r = null
                  , i = (20 === t || 28 === t) && e >= 32 && e <= 47
                  , a = (23 === t || 31 === t) && e >= 33 && e <= 35;
                if (!i && !a)
                    return !1;
                if (t === this.lastCmdA && e === this.lastCmdB)
                    return this.lastCmdA = null,
                    this.lastCmdB = null,
                    f.log("DEBUG", "Repeated command (" + p([t, e]) + ") is dropped"),
                    !0;
                r = 20 === t || 23 === t ? 1 : 2;
                var n = this.channels[r - 1];
                return 20 === t || 28 === t ? 32 === e ? n.ccRCL() : 33 === e ? n.ccBS() : 34 === e ? n.ccAOF() : 35 === e ? n.ccAON() : 36 === e ? n.ccDER() : 37 === e ? n.ccRU(2) : 38 === e ? n.ccRU(3) : 39 === e ? n.ccRU(4) : 40 === e ? n.ccFON() : 41 === e ? n.ccRDC() : 42 === e ? n.ccTR() : 43 === e ? n.ccRTD() : 44 === e ? n.ccEDM() : 45 === e ? n.ccCR() : 46 === e ? n.ccENM() : 47 === e && n.ccEOC() : n.ccTO(e - 32),
                this.lastCmdA = t,
                this.lastCmdB = e,
                this.currChNr = r,
                !0
            }
            ,
            t.prototype.parseMidrow = function(t, e) {
                var r = null;
                if ((17 === t || 25 === t) && e >= 32 && e <= 47) {
                    if ((r = 17 === t ? 1 : 2) !== this.currChNr)
                        return f.log("ERROR", "Mismatch channel in midrow parsing"),
                        !1;
                    return this.channels[r - 1].ccMIDROW(e),
                    f.log("DEBUG", "MIDROW (" + p([t, e]) + ")"),
                    !0
                }
                return !1
            }
            ,
            t.prototype.parsePAC = function(t, e) {
                var r = null
                  , i = null
                  , a = (t >= 17 && t <= 23 || t >= 25 && t <= 31) && e >= 64 && e <= 127
                  , n = (16 === t || 24 === t) && e >= 64 && e <= 95;
                if (!a && !n)
                    return !1;
                if (t === this.lastCmdA && e === this.lastCmdB)
                    return this.lastCmdA = null,
                    this.lastCmdB = null,
                    !0;
                r = t <= 23 ? 1 : 2,
                i = e >= 64 && e <= 95 ? 1 === r ? l[t] : d[t] : 1 === r ? u[t] : c[t];
                var o = this.interpretPAC(i, e);
                return this.channels[r - 1].setPAC(o),
                this.lastCmdA = t,
                this.lastCmdB = e,
                this.currChNr = r,
                !0
            }
            ,
            t.prototype.interpretPAC = function(t, e) {
                var r = e
                  , i = {
                    color: null,
                    italics: !1,
                    indent: null,
                    underline: !1,
                    row: t
                };
                return r = e > 95 ? e - 96 : e - 64,
                i.underline = 1 == (1 & r),
                r <= 13 ? i.color = ["white", "green", "blue", "cyan", "red", "yellow", "magenta", "white"][Math.floor(r / 2)] : r <= 15 ? (i.italics = !0,
                i.color = "white") : i.indent = 4 * Math.floor((r - 16) / 2),
                i
            }
            ,
            t.prototype.parseChars = function(t, e) {
                var r = null
                  , i = null
                  , a = null;
                if (t >= 25 ? (r = 2,
                a = t - 8) : (r = 1,
                a = t),
                a >= 17 && a <= 19) {
                    var o = e;
                    o = 17 === a ? e + 80 : 18 === a ? e + 112 : e + 144,
                    f.log("INFO", "Special char '" + n(o) + "' in channel " + r),
                    i = [o]
                } else
                    t >= 32 && t <= 127 && (i = 0 === e ? [t] : [t, e]);
                if (i) {
                    var s = p(i);
                    f.log("DEBUG", "Char codes =  " + s.join(",")),
                    this.lastCmdA = null,
                    this.lastCmdB = null
                }
                return i
            }
            ,
            t.prototype.parseBackgroundAttributes = function(t, e) {
                var r = void 0
                  , i = void 0
                  , a = void 0
                  , n = void 0
                  , o = (16 === t || 24 === t) && e >= 32 && e <= 47
                  , s = (23 === t || 31 === t) && e >= 45 && e <= 47;
                return !(!o && !s) && (r = {},
                16 === t || 24 === t ? (i = Math.floor((e - 32) / 2),
                r.background = h[i],
                e % 2 == 1 && (r.background = r.background + "_semi")) : 45 === e ? r.background = "transparent" : (r.foreground = "black",
                47 === e && (r.underline = !0)),
                a = t < 24 ? 1 : 2,
                n = this.channels[a - 1],
                n.setBkgData(r),
                this.lastCmdA = null,
                this.lastCmdB = null,
                !0)
            }
            ,
            t.prototype.reset = function() {
                for (var t = 0; t < this.channels.length; t++)
                    this.channels[t] && this.channels[t].reset();
                this.lastCmdA = null,
                this.lastCmdB = null
            }
            ,
            t.prototype.cueSplitAtTime = function(t) {
                for (var e = 0; e < this.channels.length; e++)
                    this.channels[e] && this.channels[e].cueSplitAtTime(t)
            }
            ,
            t
        }();
        e.a = E
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        var a = function() {
            function t(e, r) {
                i(this, t),
                this.timelineController = e,
                this.trackName = r,
                this.startTime = null,
                this.endTime = null,
                this.screen = null
            }
            return t.prototype.dispatchCue = function() {
                null !== this.startTime && (this.timelineController.addCues(this.trackName, this.startTime, this.endTime, this.screen),
                this.startTime = null)
            }
            ,
            t.prototype.newCue = function(t, e, r) {
                (null === this.startTime || this.startTime > t) && (this.startTime = t),
                this.endTime = e,
                this.screen = r,
                this.timelineController.createCaptionsTrack(this.trackName)
            }
            ,
            t
        }();
        e.a = a
    }
    , function(t, e, r) {
        "use strict";
        var i = r(3)
          , a = r(28)
          , n = r(9)
          , o = function(t, e, r) {
            return t.substr(r || 0, e.length) === e
        }
          , s = function(t) {
            var e = parseInt(t.substr(-3))
              , r = parseInt(t.substr(-6, 2))
              , a = parseInt(t.substr(-9, 2))
              , n = t.length > 9 ? parseInt(t.substr(0, t.indexOf(":"))) : 0;
            return Object(i.a)(e) && Object(i.a)(r) && Object(i.a)(a) && Object(i.a)(n) ? (e += 1e3 * r,
            e += 6e4 * a,
            e += 36e5 * n) : -1
        }
          , l = function(t) {
            for (var e = 5381, r = t.length; r; )
                e = 33 * e ^ t.charCodeAt(--r);
            return (e >>> 0).toString()
        }
          , u = function(t, e, r) {
            var i = t[e]
              , a = t[i.prevCC];
            if (!a || !a.new && i.new)
                return t.ccOffset = t.presentationOffset = i.start,
                void (i.new = !1);
            for (; a && a.new; )
                t.ccOffset += i.start - a.start,
                i.new = !1,
                i = a,
                a = t[i.prevCC];
            t.presentationOffset = r
        }
          , d = {
            parse: function(t, e, r, i, d, c) {
                var h = /\r\n|\n\r|\n|\r/g
                  , f = Object(n.b)(new Uint8Array(t)).trim().replace(h, "\n").split("\n")
                  , p = "00:00.000"
                  , g = 0
                  , v = 0
                  , y = 0
                  , m = []
                  , b = void 0
                  , E = !0
                  , T = new a.a;
                T.oncue = function(t) {
                    var e = r[i]
                      , a = r.ccOffset;
                    e && e.new && (void 0 !== v ? a = r.ccOffset = e.start : u(r, i, y)),
                    y && (a = y + r.ccOffset - r.presentationOffset),
                    t.startTime += a - v,
                    t.endTime += a - v,
                    t.id = l(t.startTime.toString()) + l(t.endTime.toString()) + l(t.text),
                    t.text = decodeURIComponent(encodeURIComponent(t.text)),
                    t.endTime > 0 && m.push(t)
                }
                ,
                T.onparsingerror = function(t) {
                    b = t
                }
                ,
                T.onflush = function() {
                    if (b && c)
                        return void c(b);
                    d(m)
                }
                ,
                f.forEach(function(t) {
                    if (E) {
                        if (o(t, "X-TIMESTAMP-MAP=")) {
                            E = !1,
                            t.substr(16).split(",").forEach(function(t) {
                                o(t, "LOCAL:") ? p = t.substr(6) : o(t, "MPEGTS:") && (g = parseInt(t.substr(7)))
                            });
                            try {
                                e = e < 0 ? e + 8589934592 : e,
                                g -= e,
                                v = s(p) / 1e3,
                                y = g / 9e4,
                                -1 === v && (b = new Error("Malformed X-TIMESTAMP-MAP: " + t))
                            } catch (e) {
                                b = new Error("Malformed X-TIMESTAMP-MAP: " + t)
                            }
                            return
                        }
                        "" === t && (E = !1)
                    }
                    T.parse(t + "\n")
                }),
                T.flush()
            }
        };
        e.a = d
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        function o(t) {
            for (var e = [], r = 0; r < t.length; r++)
                "subtitles" === t[r].kind && e.push(t[r]);
            return e
        }
        var s = r(1)
          , l = r(4)
          , u = r(0)
          , d = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , c = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, s.a.MEDIA_ATTACHED, s.a.MEDIA_DETACHING, s.a.MANIFEST_LOADING, s.a.MANIFEST_LOADED, s.a.SUBTITLE_TRACK_LOADED));
                return n.tracks = [],
                n.trackId = -1,
                n.media = null,
                n.subtitleDisplay = !0,
                n
            }
            return n(e, t),
            e.prototype._onTextTracksChanged = function() {
                if (this.media) {
                    for (var t = -1, e = o(this.media.textTracks), r = 0; r < e.length; r++)
                        if ("hidden" === e[r].mode)
                            t = r;
                        else if ("showing" === e[r].mode) {
                            t = r;
                            break
                        }
                    this.subtitleTrack = t
                }
            }
            ,
            e.prototype.destroy = function() {
                l.a.prototype.destroy.call(this)
            }
            ,
            e.prototype.onMediaAttached = function(t) {
                var e = this;
                this.media = t.media,
                this.media && (this.queuedDefaultTrack && (this.subtitleTrack = this.queuedDefaultTrack,
                delete this.queuedDefaultTrack),
                this.trackChangeListener = this._onTextTracksChanged.bind(this),
                this.useTextTrackPolling = !(this.media.textTracks && "onchange"in this.media.textTracks),
                this.useTextTrackPolling ? this.subtitlePollingInterval = setInterval(function() {
                    e.trackChangeListener()
                }, 500) : this.media.textTracks.addEventListener("change", this.trackChangeListener))
            }
            ,
            e.prototype.onMediaDetaching = function() {
                this.media && (this.useTextTrackPolling ? clearInterval(this.subtitlePollingInterval) : this.media.textTracks.removeEventListener("change", this.trackChangeListener),
                this.media = null)
            }
            ,
            e.prototype.onManifestLoading = function() {
                this.tracks = [],
                this.trackId = -1
            }
            ,
            e.prototype.onManifestLoaded = function(t) {
                var e = this
                  , r = t.subtitles || [];
                this.tracks = r,
                this.trackId = -1,
                this.hls.trigger(s.a.SUBTITLE_TRACKS_UPDATED, {
                    subtitleTracks: r
                }),
                r.forEach(function(t) {
                    t.default && (e.media ? e.subtitleTrack = t.id : e.queuedDefaultTrack = t.id)
                })
            }
            ,
            e.prototype.onTick = function() {
                var t = this.trackId
                  , e = this.tracks[t];
                if (e) {
                    var r = e.details;
                    r && !r.live || (u.b.log("(re)loading playlist for subtitle track " + t),
                    this.hls.trigger(s.a.SUBTITLE_TRACK_LOADING, {
                        url: e.url,
                        id: t
                    }))
                }
            }
            ,
            e.prototype.onSubtitleTrackLoaded = function(t) {
                var e = this;
                t.id < this.tracks.length && (u.b.log("subtitle track " + t.id + " loaded"),
                this.tracks[t.id].details = t.details,
                t.details.live && !this.timer && (this.timer = setInterval(function() {
                    e.onTick()
                }, 1e3 * t.details.targetduration, this)),
                !t.details.live && this.timer && this._stopTimer())
            }
            ,
            e.prototype.setSubtitleTrackInternal = function(t) {
                var e = this.hls
                  , r = this.tracks;
                if (!("number" != typeof t || t < -1 || t >= r.length) && (this._stopTimer(),
                this.trackId = t,
                u.b.log("switching to subtitle track " + t),
                e.trigger(s.a.SUBTITLE_TRACK_SWITCH, {
                    id: t
                }),
                -1 !== t)) {
                    var i = r[t]
                      , a = i.details;
                    a && !a.live || (u.b.log("(re)loading playlist for subtitle track " + t),
                    e.trigger(s.a.SUBTITLE_TRACK_LOADING, {
                        url: i.url,
                        id: t
                    }))
                }
            }
            ,
            e.prototype._stopTimer = function() {
                this.timer && (clearInterval(this.timer),
                this.timer = null)
            }
            ,
            e.prototype._toggleTrackModes = function(t) {
                var e = this.media
                  , r = this.subtitleDisplay
                  , i = this.trackId;
                if (e) {
                    var a = o(e.textTracks);
                    if (-1 === t)
                        [].slice.call(a).forEach(function(t) {
                            t.mode = "disabled"
                        });
                    else {
                        var n = a[i];
                        n && (n.mode = "disabled")
                    }
                    var s = a[t];
                    s && (s.mode = r ? "showing" : "hidden")
                }
            }
            ,
            d(e, [{
                key: "subtitleTracks",
                get: function() {
                    return this.tracks
                }
            }, {
                key: "subtitleTrack",
                get: function() {
                    return this.trackId
                },
                set: function(t) {
                    this.trackId !== t && (this._toggleTrackModes(t),
                    this.setSubtitleTrackInternal(t))
                }
            }]),
            e
        }(l.a);
        e.a = c
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(1)
          , s = r(0)
          , l = r(14)
          , u = r(10)
          , d = window
          , c = d.performance
          , h = {
            STOPPED: "STOPPED",
            IDLE: "IDLE",
            KEY_LOADING: "KEY_LOADING",
            FRAG_LOADING: "FRAG_LOADING"
        }
          , f = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, o.a.MEDIA_ATTACHED, o.a.ERROR, o.a.KEY_LOADED, o.a.FRAG_LOADED, o.a.SUBTITLE_TRACKS_UPDATED, o.a.SUBTITLE_TRACK_SWITCH, o.a.SUBTITLE_TRACK_LOADED, o.a.SUBTITLE_FRAG_PROCESSED));
                return n.config = r.config,
                n.vttFragSNsProcessed = {},
                n.vttFragQueues = void 0,
                n.currentlyProcessing = null,
                n.state = h.STOPPED,
                n.currentTrackId = -1,
                n.decrypter = new l.a(r.observer,r.config),
                n
            }
            return n(e, t),
            e.prototype.onHandlerDestroyed = function() {
                this.state = h.STOPPED
            }
            ,
            e.prototype.clearVttFragQueues = function() {
                var t = this;
                this.vttFragQueues = {},
                this.tracks.forEach(function(e) {
                    t.vttFragQueues[e.id] = []
                })
            }
            ,
            e.prototype.nextFrag = function() {
                if (null === this.currentlyProcessing && this.currentTrackId > -1 && this.vttFragQueues[this.currentTrackId].length) {
                    var t = this.currentlyProcessing = this.vttFragQueues[this.currentTrackId].shift();
                    this.fragCurrent = t,
                    this.hls.trigger(o.a.FRAG_LOADING, {
                        frag: t
                    }),
                    this.state = h.FRAG_LOADING
                }
            }
            ,
            e.prototype.onSubtitleFragProcessed = function(t) {
                t.success && this.vttFragSNsProcessed[t.frag.trackId].push(t.frag.sn),
                this.currentlyProcessing = null,
                this.state = h.IDLE,
                this.nextFrag()
            }
            ,
            e.prototype.onMediaAttached = function() {
                this.state = h.IDLE
            }
            ,
            e.prototype.onError = function(t) {
                var e = t.frag;
                e && "subtitle" !== e.type || this.currentlyProcessing && (this.currentlyProcessing = null,
                this.nextFrag())
            }
            ,
            e.prototype.doTick = function() {
                var t = this;
                switch (this.state) {
                case h.IDLE:
                    var e = this.tracks
                      , r = this.currentTrackId
                      , i = this.vttFragSNsProcessed[r]
                      , a = this.vttFragQueues[r]
                      , n = this.currentlyProcessing ? this.currentlyProcessing.sn : -1
                      , l = function(t) {
                        return i.indexOf(t.sn) > -1
                    }
                      , u = function(t) {
                        return a.some(function(e) {
                            return e.sn === t.sn
                        })
                    };
                    if (!e)
                        break;
                    var d;
                    if (r < e.length && (d = e[r].details),
                    void 0 === d)
                        break;
                    d.fragments.forEach(function(e) {
                        l(e) || e.sn === n || u(e) || (e.encrypted ? (s.b.log("Loading key for " + e.sn),
                        t.state = h.KEY_LOADING,
                        t.hls.trigger(o.a.KEY_LOADING, {
                            frag: e
                        })) : (e.trackId = r,
                        a.push(e),
                        t.nextFrag()))
                    })
                }
            }
            ,
            e.prototype.onSubtitleTracksUpdated = function(t) {
                var e = this;
                s.b.log("subtitle tracks updated"),
                this.tracks = t.subtitleTracks,
                this.clearVttFragQueues(),
                this.vttFragSNsProcessed = {},
                this.tracks.forEach(function(t) {
                    e.vttFragSNsProcessed[t.id] = []
                })
            }
            ,
            e.prototype.onSubtitleTrackSwitch = function(t) {
                if (this.currentTrackId = t.id,
                this.tracks && -1 !== this.currentTrackId) {
                    var e = this.tracks[this.currentTrackId];
                    e && e.details && this.tick()
                }
            }
            ,
            e.prototype.onSubtitleTrackLoaded = function() {
                this.tick()
            }
            ,
            e.prototype.onKeyLoaded = function() {
                this.state === h.KEY_LOADING && (this.state = h.IDLE,
                this.tick())
            }
            ,
            e.prototype.onFragLoaded = function(t) {
                var e = this.fragCurrent
                  , r = t.frag.decryptdata
                  , i = t.frag
                  , a = this.hls;
                if (this.state === h.FRAG_LOADING && e && "subtitle" === t.frag.type && e.sn === t.frag.sn && t.payload.byteLength > 0 && null != r && null != r.key && "AES-128" === r.method) {
                    var n = void 0;
                    try {
                        n = c.now()
                    } catch (t) {
                        n = Date.now()
                    }
                    this.decrypter.decrypt(t.payload, r.key.buffer, r.iv.buffer, function(t) {
                        var e = void 0;
                        try {
                            e = c.now()
                        } catch (t) {
                            e = Date.now()
                        }
                        a.trigger(o.a.FRAG_DECRYPTED, {
                            frag: i,
                            payload: t,
                            stats: {
                                tstart: n,
                                tdecrypt: e
                            }
                        })
                    })
                }
            }
            ,
            e
        }(u.a);
        e.a = f
    }
    , function(t, e, r) {
        "use strict";
        function i(t, e) {
            if (!(t instanceof e))
                throw new TypeError("Cannot call a class as a function")
        }
        function a(t, e) {
            if (!t)
                throw new ReferenceError("this hasn't been initialised - super() hasn't been called");
            return !e || "object" != typeof e && "function" != typeof e ? t : e
        }
        function n(t, e) {
            if ("function" != typeof e && null !== e)
                throw new TypeError("Super expression must either be null or a function, not " + typeof e);
            t.prototype = Object.create(e && e.prototype, {
                constructor: {
                    value: t,
                    enumerable: !1,
                    writable: !0,
                    configurable: !0
                }
            }),
            e && (Object.setPrototypeOf ? Object.setPrototypeOf(t, e) : t.__proto__ = e)
        }
        var o = r(4)
          , s = r(1)
          , l = r(2)
          , u = r(0)
          , d = function() {
            function t(t, e) {
                for (var r = 0; r < e.length; r++) {
                    var i = e[r];
                    i.enumerable = i.enumerable || !1,
                    i.configurable = !0,
                    "value"in i && (i.writable = !0),
                    Object.defineProperty(t, i.key, i)
                }
            }
            return function(e, r, i) {
                return r && t(e.prototype, r),
                i && t(e, i),
                e
            }
        }()
          , c = window
          , h = c.XMLHttpRequest
          , f = {
            WIDEVINE: "com.widevine.alpha",
            PLAYREADY: "com.microsoft.playready"
        }
          , p = function(t, e, r) {
            var i = {
                videoCapabilities: []
            };
            return e.forEach(function(t) {
                i.videoCapabilities.push({
                    contentType: 'video/mp4; codecs="' + t + '"'
                })
            }),
            [i]
        }
          , g = function(t, e, r) {
            switch (t) {
            case f.WIDEVINE:
                return p(0, r);
            default:
                throw Error("Unknown key-system: " + t)
            }
        }
          , v = function(t) {
            function e(r) {
                i(this, e);
                var n = a(this, t.call(this, r, s.a.MEDIA_ATTACHED, s.a.MANIFEST_PARSED));
                return n._widevineLicenseUrl = r.config.widevineLicenseUrl,
                n._licenseXhrSetup = r.config.licenseXhrSetup,
                n._emeEnabled = r.config.emeEnabled,
                n._requestMediaKeySystemAccess = r.config.requestMediaKeySystemAccessFunc,
                n._mediaKeysList = [],
                n._media = null,
                n._hasSetMediaKeys = !1,
                n._isMediaEncrypted = !1,
                n._requestLicenseFailureCount = 0,
                n
            }
            return n(e, t),
            e.prototype.getLicenseServerUrl = function(t) {
                var e = void 0;
                switch (t) {
                case f.WIDEVINE:
                    e = this._widevineLicenseUrl;
                    break;
                default:
                    e = null
                }
                return e || (u.b.error('No license server URL configured for key-system "' + t + '"'),
                this.hls.trigger(s.a.ERROR, {
                    type: l.b.KEY_SYSTEM_ERROR,
                    details: l.a.KEY_SYSTEM_LICENSE_REQUEST_FAILED,
                    fatal: !0
                })),
                e
            }
            ,
            e.prototype._attemptKeySystemAccess = function(t, e, r) {
                var i = this
                  , a = g(t, 0, r);
                if (!a)
                    return void u.b.warn("Can not create config for key-system (maybe because platform is not supported):", t);
                u.b.log("Requesting encrypted media key-system access"),
                this.requestMediaKeySystemAccess(t, a).then(function(e) {
                    i._onMediaKeySystemAccessObtained(t, e)
                }).catch(function(e) {
                    u.b.error('Failed to obtain key-system "' + t + '" access:', e)
                })
            }
            ,
            e.prototype._onMediaKeySystemAccessObtained = function(t, e) {
                var r = this;
                u.b.log('Access for key-system "' + t + '" obtained');
                var i = {
                    mediaKeys: null,
                    mediaKeysSession: null,
                    mediaKeysSessionInitialized: !1,
                    mediaKeySystemAccess: e,
                    mediaKeySystemDomain: t
                };
                this._mediaKeysList.push(i),
                e.createMediaKeys().then(function(e) {
                    i.mediaKeys = e,
                    u.b.log('Media-keys created for key-system "' + t + '"'),
                    r._onMediaKeysCreated()
                }).catch(function(t) {
                    u.b.error("Failed to create media-keys:", t)
                })
            }
            ,
            e.prototype._onMediaKeysCreated = function() {
                var t = this;
                this._mediaKeysList.forEach(function(e) {
                    e.mediaKeysSession || (e.mediaKeysSession = e.mediaKeys.createSession(),
                    t._onNewMediaKeySession(e.mediaKeysSession))
                })
            }
            ,
            e.prototype._onNewMediaKeySession = function(t) {
                var e = this;
                u.b.log("New key-system session " + t.sessionId),
                t.addEventListener("message", function(r) {
                    e._onKeySessionMessage(t, r.message)
                }, !1)
            }
            ,
            e.prototype._onKeySessionMessage = function(t, e) {
                u.b.log("Got EME message event, creating license request"),
                this._requestLicense(e, function(e) {
                    u.b.log("Received license data, updating key-session"),
                    t.update(e)
                })
            }
            ,
            e.prototype._onMediaEncrypted = function(t, e) {
                u.b.log('Media is encrypted using "' + t + '" init data type'),
                this._isMediaEncrypted = !0,
                this._mediaEncryptionInitDataType = t,
                this._mediaEncryptionInitData = e,
                this._attemptSetMediaKeys(),
                this._generateRequestWithPreferredKeySession()
            }
            ,
            e.prototype._attemptSetMediaKeys = function() {
                if (!this._hasSetMediaKeys) {
                    var t = this._mediaKeysList[0];
                    if (!t || !t.mediaKeys)
                        return u.b.error("Fatal: Media is encrypted but no CDM access or no keys have been obtained yet"),
                        void this.hls.trigger(s.a.ERROR, {
                            type: l.b.KEY_SYSTEM_ERROR,
                            details: l.a.KEY_SYSTEM_NO_KEYS,
                            fatal: !0
                        });
                    u.b.log("Setting keys for encrypted media"),
                    this._media.setMediaKeys(t.mediaKeys),
                    this._hasSetMediaKeys = !0
                }
            }
            ,
            e.prototype._generateRequestWithPreferredKeySession = function() {
                var t = this
                  , e = this._mediaKeysList[0];
                if (!e)
                    return u.b.error("Fatal: Media is encrypted but not any key-system access has been obtained yet"),
                    void this.hls.trigger(s.a.ERROR, {
                        type: l.b.KEY_SYSTEM_ERROR,
                        details: l.a.KEY_SYSTEM_NO_ACCESS,
                        fatal: !0
                    });
                if (e.mediaKeysSessionInitialized)
                    return void u.b.warn("Key-Session already initialized but requested again");
                var r = e.mediaKeysSession;
                r || (u.b.error("Fatal: Media is encrypted but no key-session existing"),
                this.hls.trigger(s.a.ERROR, {
                    type: l.b.KEY_SYSTEM_ERROR,
                    details: l.a.KEY_SYSTEM_NO_SESSION,
                    fatal: !0
                }));
                var i = this._mediaEncryptionInitDataType
                  , a = this._mediaEncryptionInitData;
                u.b.log('Generating key-session request for "' + i + '" init data type'),
                e.mediaKeysSessionInitialized = !0,
                r.generateRequest(i, a).then(function() {
                    u.b.debug("Key-session generation succeeded")
                }).catch(function(e) {
                    u.b.error("Error generating key-session request:", e),
                    t.hls.trigger(s.a.ERROR, {
                        type: l.b.KEY_SYSTEM_ERROR,
                        details: l.a.KEY_SYSTEM_NO_SESSION,
                        fatal: !1
                    })
                })
            }
            ,
            e.prototype._createLicenseXhr = function(t, e, r) {
                var i = new h
                  , a = this._licenseXhrSetup;
                try {
                    if (a)
                        try {
                            a(i, t)
                        } catch (e) {
                            i.open("POST", t, !0),
                            a(i, t)
                        }
                    i.readyState || i.open("POST", t, !0)
                } catch (t) {
                    return u.b.error("Error setting up key-system license XHR", t),
                    void this.hls.trigger(s.a.ERROR, {
                        type: l.b.KEY_SYSTEM_ERROR,
                        details: l.a.KEY_SYSTEM_LICENSE_REQUEST_FAILED,
                        fatal: !0
                    })
                }
                return i.responseType = "arraybuffer",
                i.onreadystatechange = this._onLicenseRequestReadyStageChange.bind(this, i, t, e, r),
                i
            }
            ,
            e.prototype._onLicenseRequestReadyStageChange = function(t, e, r, i) {
                switch (t.readyState) {
                case 4:
                    if (200 === t.status)
                        this._requestLicenseFailureCount = 0,
                        u.b.log("License request succeeded"),
                        i(t.response);
                    else {
                        if (u.b.error("License Request XHR failed (" + e + "). Status: " + t.status + " (" + t.statusText + ")"),
                        ++this._requestLicenseFailureCount <= 3) {
                            var a = 3 - this._requestLicenseFailureCount + 1;
                            return u.b.warn("Retrying license request, " + a + " attempts left"),
                            void this._requestLicense(r, i)
                        }
                        this.hls.trigger(s.a.ERROR, {
                            type: l.b.KEY_SYSTEM_ERROR,
                            details: l.a.KEY_SYSTEM_LICENSE_REQUEST_FAILED,
                            fatal: !0
                        })
                    }
                }
            }
            ,
            e.prototype._generateLicenseRequestChallenge = function(t, e) {
                var r = void 0;
                return t.mediaKeySystemDomain === f.PLAYREADY ? u.b.error("PlayReady is not supported (yet)") : t.mediaKeySystemDomain === f.WIDEVINE ? r = e : u.b.error("Unsupported key-system:", t.mediaKeySystemDomain),
                r
            }
            ,
            e.prototype._requestLicense = function(t, e) {
                u.b.log("Requesting content license for key-system");
                var r = this._mediaKeysList[0];
                if (!r)
                    return u.b.error("Fatal error: Media is encrypted but no key-system access has been obtained yet"),
                    void this.hls.trigger(s.a.ERROR, {
                        type: l.b.KEY_SYSTEM_ERROR,
                        details: l.a.KEY_SYSTEM_NO_ACCESS,
                        fatal: !0
                    });
                var i = this.getLicenseServerUrl(r.mediaKeySystemDomain)
                  , a = this._createLicenseXhr(i, t, e);
                u.b.log("Sending license request to URL: " + i),
                a.send(this._generateLicenseRequestChallenge(r, t))
            }
            ,
            e.prototype.onMediaAttached = function(t) {
                var e = this;
                if (this._emeEnabled) {
                    var r = t.media;
                    this._media = r,
                    r.addEventListener("encrypted", function(t) {
                        e._onMediaEncrypted(t.initDataType, t.initData)
                    })
                }
            }
            ,
            e.prototype.onManifestParsed = function(t) {
                if (this._emeEnabled) {
                    var e = t.levels.map(function(t) {
                        return t.audioCodec
                    })
                      , r = t.levels.map(function(t) {
                        return t.videoCodec
                    });
                    this._attemptKeySystemAccess(f.WIDEVINE, e, r)
                }
            }
            ,
            d(e, [{
                key: "requestMediaKeySystemAccess",
                get: function() {
                    if (!this._requestMediaKeySystemAccess)
                        throw new Error("No requestMediaKeySystemAccess function configured");
                    return this._requestMediaKeySystemAccess
                }
            }]),
            e
        }(o.a);
        e.a = v
    }
    , function(t, e, r) {
        "use strict";
        r.d(e, "a", function() {
            return i
        });
        var i = function() {
            return "undefined" != typeof window && window.navigator && window.navigator.requestMediaKeySystemAccess ? window.navigator.requestMediaKeySystemAccess.bind(window.navigator) : null
        }()
    }
    , function(t, e) {
        /*! http://mths.be/endswith v0.2.0 by @mathias */
        String.prototype.endsWith || function() {
            "use strict";
            var t = function() {
                try {
                    var t = {}
                      , e = Object.defineProperty
                      , r = e(t, t, t) && e
                } catch (t) {}
                return r
            }()
              , e = {}.toString
              , r = function(t) {
                if (null == this)
                    throw TypeError();
                var r = String(this);
                if (t && "[object RegExp]" == e.call(t))
                    throw TypeError();
                var i = r.length
                  , a = String(t)
                  , n = a.length
                  , o = i;
                if (arguments.length > 1) {
                    var s = arguments[1];
                    void 0 !== s && (o = s ? Number(s) : 0) != o && (o = 0)
                }
                var l = Math.min(Math.max(o, 0), i)
                  , u = l - n;
                if (u < 0)
                    return !1;
                for (var d = -1; ++d < n; )
                    if (r.charCodeAt(u + d) != a.charCodeAt(d))
                        return !1;
                return !0
            };
            t ? t(String.prototype, "endsWith", {
                value: r,
                configurable: !0,
                writable: !0
            }) : String.prototype.endsWith = r
        }()
    }
    ]).default
});
//# sourceMappingURL=hls.min.js.map
